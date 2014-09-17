=============================
Horizon Swift Standalone (OpenStack Dashboard)
=============================

Overview: 
   * Decouple Horizon from the mandatory component Nova and integrate with Swift standalone to provide storage as a service solution 
   * Aditional features into Horizon – Swift access url generation 

Customizations done to horizon:
 * Unregister horizon panels under Admin/project dashboards apart from swift perspective 
 * Project create/update requires resource quota to be configured as mandatory. Fixed quota to be non mandatory and hided on project create/update 
 * Under Resource & Usage panel, removed 'View Usage' option which is refering to Nova metrics. 

Swift temporary access URL generation via Horizon: 
  Allows the creation of URLs to provide temporary access to swift objects. This may be handy when need to provide download link for large objects from a Swift account which does not have public access. A temporary URL is the typical URL associated with an object, with two additional query parameters: 
  * Expire Time(In sec) - Time Duration for a swift object access url to be alive 
  * Temp-Auth-Key - A cryptographic signature 
