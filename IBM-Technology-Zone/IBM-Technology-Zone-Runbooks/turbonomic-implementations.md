# Reservations Optimized by IBM Turbonomic

IBM Technology Zone monitors reservations with IBM Turbonomic but certain reservation that are for self-education and testing purposes are optimized based on usage to free up idle resources and improve our users experience.

The purpose options self-education and test can be found on every IBM Technology Zone environment reservation form from the Purpose field drop-down list.

![purpose types](https://github.com/IBM/itz-support-public/blob/main/IBM-Technology-Zone/IBM-Technology-Zone-Runbooks/Images/purposetypes.png)


How our Turbonomic system is working:

- Daily at 1 AM (local timezone) IBM Turbonomic will process resizing actions
- Turbonomic analyzes historical utilization and will resize vCPU and vMem up or down when it identified historically heavy or light utilization respectively
- This automation is actioned on for reservations that are NOT customer facing and can be resized up if needed but currently requires [opening a support case](https://ibmsf.my.site.com/ibminternalproducts/s/createrecord/NewCase?language=en_US)
