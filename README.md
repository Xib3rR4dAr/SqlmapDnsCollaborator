# SqlmapDnsCollaborator

SqlmapDnsCollaborator is a Burp Extension that lets you perform DNS exfiltration with Sqlmap with zero configuration needed. You won't need a domain name or a public IP, just a computer with Sqlmap and Burp.   
   
How you would normally perform DNS exfiltration with Sqlmap:  
1. You buy a domain name, a public IP and then you set up a server!!  
2. You run Sqlmap on that server, which performs some SQL injection on the vulnerable target.  
3. Vulnerable target sends DNS requests to your DNS server containing interesting data.  
4. DNS requests are interpreted by Sqlmap.  
  
How you are going to perform DNS exfiltration with Sqlmap and SqlmapDnsCollaborator:  
1. You open Burp on your computer and enable SqlmapDnsCollaborator.  
2. You run Sqlmap on your computer, which performs some SQL injection on the vulnerable target.  
3. Vulnerable target sends DNS requests to Burp Collaborator containing interesting data.  
4. SqlmapDnsCollaborator reads DNS requests from Burp Collaborator and sends them to Sqlmap.  
4. DNS requests are interpreted by Sqlmap.  
