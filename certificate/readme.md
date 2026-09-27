## see  as i am a admin of kubernetes cluster and a new user come for  admin role then i have share  certificates with him  

## this are the step follow by new user

# When you're creating SSL/TLS certificates, the flow is:
Private Key (.key)
       ↓
      CSR (.csr)
       ↓
Certificate (.crt / .pem) 


   ## syntax

openssl genrsa -out myuser.key 2048  ## # 1. Generate private key
openssl  req -new -key myuser.key -out myuser.csr -subj "/CN=myuser" ## # 2. Create CSR

## CSR stands for Certificate Signing Request.
A CSR contains information about the identity you want the certificate for. You generate it from the private key:
  
eg:-

openssl genrsa -out adam.key 2048
openssl req -new -key adam.key -out adam.csr -subj "/CN=adam"
