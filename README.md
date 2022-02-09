# HTTP_Req_method_per_sec_iRule
An F5 LTM iRule to gauge specific requests per sec by Method.  Default is POST, can be changed

Note, it reports the maximum Requests per second for POST methods. 
 
Two ways to see the result is:

using curl:

        curl http://<virtual IP> -X OPTIONS
        
using tmsh:

                    tmsh show ltm virtual <virtual name>
                    
                    in this case you will find it under:
                    
                    User-defined         Value
                    
                       max_posts_per_sec   4
 
 
To reset the value send a DELETE method.

        curl -v http://<virtual IP> -X DELETE
 
