# Creating a Self Signed Certificate

## Prepare and Generate the certificate using the IIS Manager

Go to the Server Certificates view
![Go to the Server Certificates view](images/1.png)

Select to Create a Self-Signed Certificate
![Select to Create a Self-Signed Certificate](images/2.png)

Specify a name and set the certificate store to Web Hosting
![Specify a name and set the certificate store to Web Hosting](images/3.png)

Select to Export the certificate
![Select to Export the certificate](images/4.png)

Give it a file location and a password, same password you would use in for instance IdentityServer
![Give it a file location and a password, same password you would use in for instance IdentityServer](images/5.png)

## Get the Certificate as a Base64 encoded string

```
var certificate = Convert.ToBase64String(File.ReadAllBytes(@"C:\Temp\DemoCert.pfx"));
```