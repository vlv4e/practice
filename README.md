Dear team, 

Please find the root cause investigation update from the latest afternoon checkpoint session. 

*Summary:* TEMENOS has confirmed the source of the 4 corrupted data entries that led to txn rejections was due the ebsence of an applicarion level restart being performed post the Friday morning core banking deployment. Only API level restarts were executed by the systems ltd engineer.

*Details:* 4 corrupted records present in T24 database table resulted in all transactions being flagged as duplicate and as a result being rejected.

Update: 

- Systems ltd has confirmed no application level restart was conducted as part of the release which led to corrupt records entering a core banking table. Only api level restarts were executed on the associated PODS.

- TEMENOS have confirmed this issue is not at a base product level  and resides within the local customization (systems ltd L3 client specific customization). They have advised an application restart should be executed after each of these categories of releases.

*Immediate Next Steps*:

- systems ltd team to apply mandated sequence of restarts to all production deployments as per  the recommended by TEMENOS. All run books require to be updated with a mandatory restart for the same when core components are included.
