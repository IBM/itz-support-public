# Accounting API

**Production**
[https://accounting.assetrepo.ibm.com](https://accounting.assetrepo.ibm.com)
([Swagger](https://accounting.assetrepo.ibm.com/swagger))

**Staging**
[https://assetrepo-staging-accounting.dal1a.ciocloud.nonprod.intranet.ibm.com](https://assetrepo-staging-accounting.dal1a.ciocloud.nonprod.intranet.ibm.com/)
([Swagger](https://assetrepo-staging-accounting.dal1a.ciocloud.nonprod.intranet.ibm.com/swagger))

**GitHub**
[https://github.ibm.com/itz/accounting](https://github.ibm.com/itz/accounting)

---

### Onboarding

- Acquire an API Token by navigating to the Asset Repo profile page [https://assetrepo.ibm.com/my/profile](https://assetrepo.ibm.com/my/profile). This token can be used for all Asset Repo API endpoints as a Bearer token (using a service id is suggested).
- Get your unique origin and provider information from [Brooke Jones](mailto:brooke.jones@ibm.com) or [Benjamin Foulkes](mailto:ben.foulkes@ca.ibm.com)
- Submit your reservation accounting journal entries via a POST request at a regular cadence or at reservation time.
- Review your data in the dashboard

---

### Accounting API schema

    oid: {
      type: "string",
      maxLength: 100,
      allowNull: false,
      description: "Unique identifier from origin",
    },
    cid: {
      type: "string",
      maxLength: 100,
      allowNull: true,
      description: "Optional unique identifier from origin for the content or collection",
    },
    label: {
      type: "string",
      maxLength: 1024,
      allowNull: true,
      description: "A label or name to attach to this journal entry",
    },
    environment: {
      type: "string",
      maxLength: 255,
      allowNull: true,
      description: "environment/template id/name",
    },
    origin: { type: "string", maxLength: 255, description: "who originated the service request" },
    provider: { type: "string", maxLength: 255, description: "who is completing this request" },
    platform: {
      type: "string",
      maxLength: 255,
      description: "Platform being provided (Azure, ROKS, Skytap)",
    },
    account: {
      type: "string",
      maxLength: 255,
      description: "Optional account being leverage for this workload",
    },
    quantity: { type: "number", defaultsTo: 1, description: "How many instances were created" },
    attendees: { type: "number", defaultsTo: 1, description: "How many people are attending" },
    cost: { type: "number", defaultsTo: 0, description: "How much does this cost" },
    purpose: { type: "string", maxLength: 255, allowNull: true, description: "Purpose for this" },
    products: { type: "json", description: "Products object.  Can be a single or multiple array" },
    opportunity: {
      type: "json",
      description: "Opportunity object. Can be a single or multiple array",
    },
    customer: { type: "json", description: "Customer object. Can be a single or multiple array" },
    iui: { type: "string", maxLength: 255, allowNull: true, description: "ibm iui/ibmid or email" },
    persona: {
      type: "string",
      maxLength: 25,
      allowNull: true,
      isIn: ["ibmer", "partner", "customer", "other", "unknown", "user", ""],
      description:
        "Optional user persona. Do NOT specify if you want auto persona and profile population",
    },
    company: {
      type: "string",
      maxLength: 1024,
      allowNull: true,
      description: "Optional user company (specified or derived from profile)",
    },
    org: {
      type: "string",
      maxLength: 100,
      allowNull: true,
      description: "Optional user org (specified or derived from profile)",
    },
    dept: {
      type: "string",
      maxLength: 100,
      allowNull: true,
      description: "Optional user dept (specified or derived from profile)",
    },
    div: {
      type: "string",
      maxLength: 100,
      allowNull: true,
      description: "Optional user div (specified or derived from profile)",
    },
    region: {
      type: "string",
      maxLength: 255,
      allowNull: true,
      description: "Optional user region (specified or derived from profile)",
    },
    country: {
      type: "string",
      maxLength: 255,
      allowNull: true,
      description: "Optional user country (specified or derived from profile)",
    },
    start: { type: "number", allowNull: true, description: "Start date/time in epoch" },
    end: { type: "number", allowNull: true, description: "End date/time in epoch" },
    owner: {
      type: "string",
      maxLength: 255,
      allowNull: true,
      description: "Record owner for updates/deletes",
    },
    notes: { type: "string", maxLength: 4096, description: "Notes and other data to log" },
    mia: {
      type: "boolean",
      defaultsTo: false,
      allowNull: true,
      description: "Tag a user as missing in action (used to stop unkonwn re-lookups)",
    }

---

### Data normalization

**Purpose**

Purpose should be one of the following values.

- Demo
- Self Education
- Other
- Proof of Concept
- Proof of Technology
- Testing
- Workshop

**Platform**

Platform is the infrastructure that you are running on. Some examples of platforms are:

- Skytap
- IBM Cloud
- Other
- Managed OpenShift (ROKS)
- VMWare Private Cloud (Cloud Lab)
- KVM Private Cloud (Fyre)
- AWS
- Azure

**Products**

Products consist of distinct UT codes which can be found in [FedCat Unified Taxonomy](https://w3.ibm.com/w3publisher/fedcat/components/unified-taxonomy). Multiple products and products levels can be specified.

For example:

    [
        {
            "utcode": "30BJ0",
            "utlevel": 30
        },
        {
            "utcode": "20B1A",
            "utlevel": 20
        }
    ]

**Origin/Provider**

Origin and Provider are unique to each pipeline and data provider. Do not just make something up. Make sure to use the assigned Origin and Provider.

**Start/End**

Start and end dates are in Unix epoch

**Persona**

Persona describe what type of user this is and should be one of the following:

- ibmer
- partner
- customer
- other
- unknown
- user

---

### Creating Journal entries

HTTP POST

    {
      "oid": "123",
      "cid": "optional-content-or-collection-id",
      "label": "entry label",
      "environment": "optional-environment-or-template-id",
      "origin": "your-unique-origin",
      "provider": "your-unique-provider",
      "platform": "some-platform",
      "account": "optional account",
      "quantity": 1,
      "attendees": 1,
      "cost": 0,
      "purpose": "some purpose",
      "iui": "iui or email address",
      "start": 0,
      "end": 0,
      "notes": "some additional notes"
    }

**Curl**

    TOKEN=YOUR_API_TOKEN
    curl -X POST "https://accounting.assetrepo.ibm.com/api/journal"  -H "Authorization: Bearer ${TOKEN}" -H  "accept: application/json" -H  "Content-Type: application/json" -d "{\"oid\":\"123\",\"cid\":\"optional-content-or-collection-id\",\"label\":\"entry label\",\"environment\":\"optional-environment-or-template-id\",\"origin\":\"your-unique-origin\",\"provider\":\"your-unique-provider\",\"platform\":\"some-platform\",\"account\":\"optional account\",\"quantity\":1,\"attendees\":1,\"cost\":0,\"purpose\":\"some purpose\",\"iui\":\"iui or email address\",\"start\":0,\"end\":0,\"notes\":\"some additional notes\"}"

**Fetch**

    let token = 'YOUR_API_TOKEN';
    let options = {
    	method: 'POST',
    	headers: {
    		'Content-Type': 'application/json',
    		`Authorization: Bearer ${token}`
    	},
    	body: JSON.stringify({
    	  "oid": "123",
        "cid": "optional-content-or-collection-id",
    	  "label": "entry label",
    	  "environment": "optional-environment-or-template-id",
    	  "origin": "your-unique-origin",
    	  "provider": "your-unique-provider",
    	  "platform": "some-platform",
    	  "account": "optional account",
    	  "quantity": 1,
    	  "attendees": 1,
    	  "cost": 0,
    	  "purpose": "some purpose",
    	  "iui": "iui or email address",
    	  "start": 0,
    	  "end": 0,
    	  "notes": "some additional notes"
    	})
    }
    fetch('https://accounting.assetrepo.ibm.com/api/journal', options)
      .then(resp => resp.json())
      .then(data => data);

---

### Updating Journal entries

HTTP PATCH

    {
    	id: UNIQUE_ID_FOR_THE_RECORD
    	...
    	only send what you need to patch
    }

**Curl**

    TOKEN=YOUR_API_TOKEN
    ID=THE_ID_OF_THE_RECORD
    curl -X PATCH "https://accounting.assetrepo.ibm.com/api/journal/${ID}" -H "Authorization: Bearer ${TOKEN}" -H  "accept: application/json" -H  "Content-Type: application/json" -d "{\"oid\":\"123\",\"cid\":\"optional-content-or-collection-id\",\"label\":\"entry label\",\"environment\":\"optional environment or template id\",\"origin\":\"your-unique-origin\",\"provider\":\"your-unique-provider\",\"platform\":\"some-platform\",\"account\":\"optional account\",\"quantity\":1,\"attendees\":1,\"cost\":0,\"purpose\":\"some purpose\",\"iui\":\"iui or email address\",\"start\":0,\"end\":0,\"notes\":\"some additional notes\"}"

**Fetch**

    let token = 'YOUR_API_TOKEN';
    let id = 'THE_ID_OF_THE_RECORD';
    let options = {
    	method: 'PATCH',
    	headers: {
    		'Content-Type': 'application/json',
    		`Authorization: Bearer ${token}`
    	},
    	body: JSON.stringify({
    	  "id": id
    	  "oid": "123",
        "cid": "optional-content-or-collection-id",
    	  "label": "entry label",
    	  "environment": "optional environment or template id",
    	  "origin": "your-unique-origin",
    	  "provider": "your-unique-provider",
    	  "platform": "some-platform",
    	  "account": "optional account",
    	  "quantity": 1,
    	  "attendees": 1,
    	  "cost": 0,
    	  "purpose": "some purpose",
    	  "iui": "iui or email address",
    	  "start": 0,
    	  "end": 0,
    	  "notes": "some additional notes"
    	})
    }
    fetch(`https://accounting.assetrepo.ibm.com/api/journal/${id}`, options)
      .then(resp => resp.json())
      .then(data => data);

---

### Deleting Journal entries

HTTP DELETE

    { id: UNIQUE_ID_FOR_THE_RECORD }

**Curl**

    TOKEN=YOUR_API_TOKEN
    ID=THE_ID_OF_THE_RECORD
    curl -X DELETE "https://accounting.assetrepo.ibm.com/api/journal/${ID}" -H "Authorization: Bearer ${TOKEN}" -H  "accept: application/json" -H  "Content-Type: application/json"

**Fetch**

    let token = 'YOUR_API_TOKEN';
    let id = 'THE_ID_OF_THE_RECORD';
    let options = {
    	method: 'DELETE',
    	headers: {
    		'Content-Type': 'application/json',
    		`Authorization: Bearer ${token}`
    	}
    }
    fetch(`https://accounting.assetrepo.ibm.com/api/journal/${id}`, options)
      .then(resp => resp.json())
      .then(data => data);

---

### Searching Journal entries

The Accounting API uses MongoDB for durable storage and leverages ElasticSearch to accelerate searches.

Use the following documentation for performing queries against SailsJS/MongoDB.

[https://sailsjs.com/documentation/reference/blueprint-api/find-where](https://sailsjs.com/documentation/reference/blueprint-api/find-where)

    HTTP GET

    https://accounting.assetrepo.ibm.com/api/journal?access_token=[YOUR_ACCESS_TOKEN]

Use the following endpoints for ElasticSearch.

    HTTP GET or POST

    https://accounting.assetrepo.ibm.com/api/journal/_search?access_token=[YOUR_ACCESS_TOKEN]
    https://accounting.assetrepo.ibm.com/api/journal/_msearch?access_token=[YOUR_ACCESS_TOKEN]

Note: Make sure to include access_token=[YOUR_ACCESS_TOKEN] in the url query string for all get requests.

---

### Architecture

![](https://raw.github.ibm.com/itz/accounting/master/data/accounting.png?token=AAAC3W3EKH6XEYJUWLQWTS3ASVVRC)
