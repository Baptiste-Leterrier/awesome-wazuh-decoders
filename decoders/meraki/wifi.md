# Decoders

```
<decoder name="cisco_meraki_wpa_auth">
    <prematch>type=wpa_auth</prematch>
</decoder>
 
<decoder name="cisco_meraki_wpa_auth">
    <parent>cisco_meraki_wpa_auth</parent>
    <regex type="pcre2">([^ ]+) events</regex>
    <order>wifi_name</order>
</decoder>
 
<decoder name="cisco_meraki_wpa_auth">
    <parent>cisco_meraki_wpa_auth</parent>
    <regex type="pcre2">events type=([^ ]+)</regex>
    <order>event_type</order>
</decoder>
 
<decoder name="cisco_meraki_wpa_auth">
    <parent>cisco_meraki_wpa_auth</parent>
    <regex type="pcre2">client_mac='([^']+)'</regex>
    <order>client_mac</order>
</decoder>
 
<decoder name="cisco_meraki_wpa_assoc">
    <prematch>type=association</prematch>
</decoder>
 
<decoder name="cisco_meraki_wpa_assoc">
    <parent>cisco_meraki_wpa_assoc</parent>
    <regex type="pcre2">([^ ]+) events</regex>
    <order>wifi_name</order>
</decoder>
 
<decoder name="cisco_meraki_wpa_assoc">
    <parent>cisco_meraki_wpa_assoc</parent>
    <regex type="pcre2">events type=([^ ]+)</regex>
    <order>event_type</order>
</decoder>
 
<decoder name="cisco_meraki_wpa_assoc">
    <parent>cisco_meraki_wpa_assoc</parent>
    <regex type="pcre2">client_mac='([^']+)'</regex>
    <order>client_mac</order>
</decoder>
 
 
<decoder name="cisco_meraki_wpa_deauth">
    <prematch>type=wpa_deauth</prematch>
</decoder>
 
<decoder name="cisco_meraki_wpa_deauth">
    <parent>cisco_meraki_wpa_deauth</parent>
    <regex type="pcre2">([^ ]+) events</regex>
    <order>wifi_name</order>
</decoder>
 
<decoder name="cisco_meraki_wpa_deauth">
    <parent>cisco_meraki_wpa_deauth</parent>
    <regex type="pcre2">events type=([^ ]+)</regex>
    <order>event_type</order>
</decoder>
 
<decoder name="cisco_meraki_wpa_deauth">
    <parent>cisco_meraki_wpa_deauth</parent>
    <regex type="pcre2">client_mac='([^']+)'</regex>
    <order>client_mac</order>
</decoder>
 
<decoder name="cisco_meraki_disassociation">
    <prematch>type=disassociation</prematch>
</decoder>
 
<decoder name="cisco_meraki_disassociation">
    <parent>cisco_meraki_disassociation</parent>
    <regex type="pcre2">reason='([^']+)</regex>
    <order>deauth_reason</order>
</decoder>
 
<decoder name="cisco_meraki_disassociation">
    <parent>cisco_meraki_disassociation</parent>
    <regex type="pcre2">([^ ]+) events</regex>
    <order>wifi_name</order>
</decoder>
 
<decoder name="cisco_meraki_disassociation">
    <parent>cisco_meraki_disassociation</parent>
    <regex type="pcre2">events type=([^ ]+)</regex>
    <order>event_type</order>
</decoder>
 
<decoder name="cisco_meraki_disassociation">
    <parent>cisco_meraki_disassociation</parent>
    <regex type="pcre2">client_mac='([^']+)'</regex>
    <order>client_mac</order>
</decoder>
```

# Alerts
```
<group name="cisco_meraki">
  <rule id="190001" level="3">
    <decoded_as>cisco_meraki_wpa_auth</decoded_as>
    <description>Wifi Authentication</description>
  </rule>
  <rule id="190002" level="3">
    <decoded_as>cisco_meraki_wpa_assoc</decoded_as>
    <description>Wifi Association</description>
  </rule>
  <rule id="190003" level="3">
    <decoded_as>cisco_meraki_wpa_deauth</decoded_as>
    <description>Wifi Deauthentication</description>
  </rule>
  <rule id="190004" level="3">
    <decoded_as>cisco_meraki_disassociation</decoded_as>
    <description>Wifi Disassociation</description>
  </rule>
</group>
```
