# api.com.gosecure
 API integration for GoSecure

https://www.gosecure.net/docs/support/help-files/api/Index.htm

Web API docs.

Having this dataset in tools such a Liongard would help us solve a couple huge gaps with this particular product.

Brightgauge Dashboard Reporting. There has never been very good reporting out of this tool, and the fact that the mailboxes (active users) are part of the configuration would allow us to provide active user metrics for our managed orgs in this system.

Alerting. We deal with lots of challenges simply due to misconfigurations that don't follow best practices. Liongard's metric and alert technology make it possible to notify teams when an tenant's settings are incorrect.

Documentation. Auto docs in IT Glue help non technical staff quickly access detailed system information.

# Sample From gosecure.net

Configuration Download
To download the complete configuration for a given domain as an XML document, enter the following statement:

curl "http://$DASHBOARD/api/config/download?token=$TOKEN&domain=domain.com"

Note that only the domain prefix needs to be specified. For example domain=GoSecure will match GoSecure.com, GoSecure.net, GoSecures.com. If no domain is specified, the resulting XML document will contain the configuration for all domains in the branded dashboard.


