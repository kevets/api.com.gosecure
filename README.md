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

You can specify the configuration download version by adding the following:

&version=2.7>2.6

 



Note: In this release, for configuration download to work properly the version specified must be 2.7 or none.

The following is an example of a XML schema download:

<configuration version="2.7" timestamp="2013-10-29T17:12:52.493">

<verifier name="benoit" uid="D2AAE5F3-B0F9-0AC9-3D22-F28C993EE270" account="">

     <Vrfy version="101.3807">

       <MetaData>

         <Editable>true</Editable>

         </MetaData>

       <LDAP defaults="ActiveDirectory">

         <Host secure="false">postal.GoSecure.com</Host>

         <HostListOrder>Shuffle</HostListOrder>

<Timeout>5</Timeout>

</LDAP>

     </Vrfy>

    </verifier>

  <domain-defaults gateway="mail.GoSecure.com" clienttls="none" emailcontinuity="false" inboundTLSDomains="" authenticator="" dsnunrestricted="false" maxmsgsize="5" spoolerduration="96" senderSpoof="false" antiSpoof="" retainblocked="false" retaindelivered="true" mbcleanup="3" token="true" balanced="false" discovery="disabled" unrecognized="bounce" odi="true" notifydiscovery="true" sessionverify="false" dhaprotection="bounce_only">

  <contentfilters/>

  <console enabled="true" quarantine="true" outbound="false" release="true" settings="true" policies="true" foreign="true" attachments="true" sender="true"/>

  </domain-defaults>  

  <outbound-defaults gateway="" clienttls="available" authenticator="" dsnunrestricted="false" maxmsgsize="unlimited" spoolerduration="2" retainblocked="false" retaindelivered="false" mphuser="unlimited" mphother="unlimited" mphuserresponse="451 Hourly outbound rate limit exceeded" mphotherresponse="550 Hourly outbound rate limit exceeded" rcptlimit="unlimited" rcptlimitresponse="451 Recipient limit exceeded for this sender" dsn="false" dsnlimit="3" sessiontls="available" annotation="none">

<contentfilters/>

<exemptrecipients/>

<tlsdomains policy="available"/>

<gateways/>

</outbound-defaults>

<groups>

<group name="SVT Group 2" uid="23a6ef94-0589-4e4e-abf6-f8321da7085a" domainname="example.com" grouppriority="2" type="outbound" gateway="encryption.example.com" timezone="" bcc="">

<annotation/>

<friends/>

<enemies/>

<categories/>

<languages/>

<extensions/>

<console enabled="" quarantine="" outbound="" release="" settings="" policies="" foreign="" attachments="" sender=""/>

</group>

<group name="SVT Group 2" uid="9d7a4b1c-9502-40e1-99b8-5e457d721930" domainname="example.com" grouppriority="3" type="inbound" gateway="mail2.example.com" timezone="" bcc="">

<annotation/>

<digest detail="inherit" format="inherit" language="inherit" frequency="inherit" order=""/>

<friends/>

<enemies/>

<categories/>

<languages/>

<extensions/>

<console enabled="" quarantine="" outbound="" release="" settings="" policies="" foreign="" attachments="" sender=""/>

</group>

</groups>

<contentfilter name="Bad Words" uid="86B88D3C-F29B-6F59-6B0E-6C26603FC18B" account="A5A659B3-6901-4D8A-B231-100C0DF2FCC0"> [{"parts":["HEADER","TEXT"],"filters":["bar","foo"], "headers":["Subject:","From:"} ]

</contentfilter>

  <contentfilter name="Another List" uid="BFE78762-1788-4DA2-B84F-3C73D3C7EF09" account="A5A659B3-6901-4D8A-B231-100C0DF2FCC0"> [{"parts":["HEADER"],"filters":["badword0","badword1"], "headers":["Subject:","Sender:"}]

</contentfilter>

     <domain name="example.com" notifydiscovery="true" account="C2F26595-29E2-764D-3519-13" emailcontinuity="false" inboundTLSDomains="" timezone="" gateway="" discovery="external" authenticator="" unrecognized="discard" dsn="false" dsnlimit="0" dsnunrestricted="false" maxmsgsize="5" odi="false" verifier="D2AAE5F3-B0F9-0AC9-3D22-F28C993EE270" outboundaccess="false" consoleaccess="true" clienttls="none" dhaprotection="bounce_only" bcc="b5e91e4a-40f6-12df-9e06-12313b001843@mail.gosecurearchive.com" balanced="false" spoolerduration="96" senderSpoof="false" antiSpoof="" emcAutoEnabled="false" emcAutoEnableDuration="15" emcautodisableduration="900000" emctestemail="" emcautodisabled="false" emcOfflineTimeout="600000"emconlinetimeout="600000">

<digest detail="red" format="html" frequency="never" order="Date-"/>

<categories>

<category name="junk" action="quarantine"/>

<category name="virus" action="quarantine"/>

<category name="adult" action="quarantine"/>

          <category name="spam" action="quarantine"/>

</categories>

<languages/>

<extensions>

<extension name="asd" action="quarantine"/>

<extension name="bat" action="quarantine"/>

<extension name="cab" action="quarantine"/>

<extension name="chm" action="quarantine"/>

<extension name="com" action="quarantine"/>

<extension name="cpl" action="quarantine"/>

<extension name="dat" action="quarantine"/>

<extension name="dll" action="quarantine"/>

<extension name="eml" action="quarantine"/>

<extension name="exe" action="quarantine"/>

<extension name="hlp" action="quarantine"/>

<extension name="hta" action="quarantine"/>

<extension name="inf" action="quarantine"/>

<extension name="lnk" action="quarantine"/>

<extension name="msi" action="quarantine"/>

<extension name="msp" action="quarantine"/>

<extension name="nws" action="quarantine"/>

<extension name="ocx" action="quarantine"/>

<extension name="pif" action="quarantine"/>

<extension name="reg" action="quarantine"/>

<extension name="scr" action="quarantine"/>

<extension name="sct" action="quarantine"/>

<extension name="shb" action="quarantine"/>

<extension name="shs" action="quarantine"/>

<extension name="vbe" action="quarantine"/>

<extension name="vbs" action="quarantine"/>

<extension name="vcd" action="quarantine"/>

<extension name="vcf" action="quarantine"/>

<extension name="wsc" action="quarantine"/>

<extension name="wsf" action="quarantine"/>

<extension name="wsh" action="quarantine"/>

<extension name="zip" action="quarantine"/>

</extensions>

<contentfilters>

<contentfilter uid="86B88D3C-F29B-6F59-6B0E-6C26603FC18B" action="quarantine"/>

<contentfilter uid="BFE78762-1788-4DA2-B84F-3C73D3C7EF09" action="quarantine"/>

</contentfilters>

<console enabled="true" quarantine="true" outbound="false" release="true" settings="true" policies="true" foreign="true" attachments="true" sender="true"/>

<mailbox name="admin" status="active" consoleaccess="" timezone="" bcc="">

<digest detail="inherit" format="inherit" frequency="inherit" order="Date-"/>

<categories/>

<languages/>

<extensions/>

</mailbox>

<mailbox name="alex" status="active" consoleaccess="" timezone="" bcc="">

<digest detail="inherit" format="inherit" frequency="inherit" order="Date-"/> <categories/><languages/><extensions/>

<groups><group type="manual">SVT Group 2</group><group type="auto">engineering</group>

<group type="auto">sales</group></groups>

</mailbox>

<mailbox name="chris" status="active" consoleaccess="" timezone="" bcc="">

<digest detail="red" format="html" frequency="daily" order="Date+"/>

<categories>

<category name="junk" action="quarantine"/>

<category name="virus" action="quarantine"/>

<category name="phish" action="quarantine"/>

<category name="adult" action="quarantine"/>

<category name="spam" action="quarantine"/>

</categories>

<languages>

<language name="BS" action="markup" markup="FOREIGN:"/>

<language name="CC" action="quarantine"/>

<language name="CE" action="quarantine"/>

<language name="CY" action="quarantine"/>

<language name="EE" action="quarantine"/>

<language name="NO" action="quarantine"/>

<language name="SE" action="quarantine"/>

<language name="ar" action="quarantine"/>

<language name="el" action="quarantine"/>

<language name="he" action="quarantine"/>

<language name="ja" action="quarantine"/>

<language name="ko" action="quarantine"/>

<language name="th" action="quarantine"/>

<language name="tr" action="quarantine"/>

<language name="zh" action="quarantine"/>

</languages>

<extensions>

<extension name="asd" action="quarantine"/>

<extension name="bat" action="quarantine"/>

<extension name="cab" action="quarantine"/>

<extension name="chm" action="quarantine"/>

<extension name="com" action="quarantine"/>

<extension name="cpl" action="quarantine"/>

<extension name="dat" action="quarantine"/>

<extension name="dll" action="quarantine"/>

<extension name="eml" action="quarantine"/>

<extension name="exe" action="quarantine"/>

<extension name="hlp" action="quarantine"/>

<extension name="hta" action="quarantine"/>

<extension name="inf" action="quarantine"/>

<extension name="lnk" action="quarantine"/>

<extension name="msi" action="quarantine"/>

<extension name="msp" action="quarantine"/>

<extension name="nws" action="quarantine"/>

<extension name="ocx" action="quarantine"/>

<extension name="reg" action="quarantine"/>

<extension name="sct" action="quarantine"/>

<extension name="shb" action="quarantine"/>

<extension name="shs" action="quarantine"/>

<extension name="vbe" action="quarantine"/>

<extension name="vbs" action="quarantine"/>

<extension name="vcd" action="quarantine"/>

<extension name="vcf" action="quarantine"/>

<extension name="wsc" action="quarantine"/>

<extension name="wsf" action="quarantine"/>

<extension name="wsh" action="quarantine"/>

<extension name="zip" action="quarantine"/>

</extensions>

<alias name="christopher"/>

</mailbox>

<mailbox name="hawaii_mom" status="active" failure="2009-07-31T22:19:27.644" consoleaccess="" timezone="" bcc="">

<digest detail="inherit" format="inherit" frequency="inherit" order=""/>

<categories/>

<languages/>

<extensions/>

</mailbox>

<mailbox name="test" status="inactive"/>

</domain>

<outbound source="1.2.3.4/32" account="a5a659b3-6901-4d8a-b231-100c0df2fcc0" timezone="" bcc="" gateway="" authenticator="" dsn="true" dsnlimit="unlimited" dsnunrestricted="true" maxmsgsize="100" spoolerduration="1" retainblocked="true" authrequired="true" mphuser="unlimited" mphother="unlimited" mphuserresponse="451 Hourly outbound rate limit exceeded" mphotherresponse="550 Hourly outbound rate limit exceeded" rcptlimit="unlimited" rcptlimitresponse="451 Recipient limit exceeded for this sender" sessiontls="none" annotation="append">

<friends/>

<enemies/>

<categories>

<category name="credit" action="markup" markup="CREDIT CARD:"/>

<category name="ssn" action="markup" markup="SOCIAL SECURITY:"/>

<category name="virus" action="quarantine"/>

<category name="phish" action="quarantine"/>

<category name="adult" action="quarantine"/>

<category name="pdf" action="quarantine"/>

<category name="bot" action="quarantine"/>

<category name="spam" action="quarantine"/>

</categories>

<languages/>

<extensions>

<extension name="asd" action="quarantine"/>

<extension name="bat" action="block"/>

<extension name="cab" action="quarantine"/>

<extension name="chm" action="quarantine"/>

<extension name="com" action="block"/>

<extension name="cpl" action="quarantine"/>

<extension name="dll" action="quarantine"/>

<extension name="exe" action="quarantine"/>

<extension name="hlp" action="quarantine"/>

<extension name="hta" action="quarantine"/>

<extension name="inf" action="quarantine"/>

<extension name="lnk" action="quarantine"/>

<extension name="msi" action="quarantine"/>

<extension name="msp" action="quarantine"/>

<extension name="nws" action="quarantine"/>

<extension name="ocx" action="quarantine"/>

<extension name="pif" action="block"/>

<extension name="reg" action="quarantine"/>

<extension name="scr" action="block"/>

<extension name="sct" action="quarantine"/>

<extension name="shb" action="quarantine"/>

<extension name="shs" action="quarantine"/>

<extension name="vbe" action="quarantine"/>

<extension name="vbs" action="quarantine"/>

<extension name="wsc" action="quarantine"/>

<extension name="wsf" action="quarantine"/>

<extension name="wsh" action="quarantine"/>

</extensions>

<contentfilters>

<contentfilter uid="52bd2714-a881-4772-acf2-efb82cf53bd7" action="quarantine"/>

</contentfilters>

<exemptrecipients/>

<tlsdomains policy="none"/>

<gateways/>

<annotation>

<p>Test Annotation message - xxxyyyzzz</p>

</annotation>

</outbound>

</configuration>