# CICD
## Github ssh set up
### Webhooks
![](images/CICD.png)
# eng99Cicd

### Testing jenkins ci

#### Github

- Open gitbash and cd into .ssh file
- `ssh-keygen -t rsa -b 4096 -C "emailaddress"` e.g ssh-keygen -t rsa -b 4096 -C "bob@hotmail.com"
> this will create a public and private key
- enter a name for the keys
- go to github repo
- click on settings 
- click deploy key
- add key <file> and copy the public key into github

![image](https://user-images.githubusercontent.com/94615905/145449161-09c6b32a-320b-4b7a-9ad4-82ecafdfa0cf.png)
  
#### Adding webjook
  
![image](https://user-images.githubusercontent.com/94615905/145450801-5ba06728-3890-450f-8924-9ee214d20fc3.png)

 url (e.g `http://35.178.35.127:8080/` ) + `github-webhook/`
 

#### Jenkins
  
- Create Job

![image](https://user-images.githubusercontent.com/94615905/145449503-c69b4b4a-e2ee-4de6-883e-57548e61c2f8.png)
  
![image](https://user-images.githubusercontent.com/94615905/145449681-0fa4bbb8-a088-425a-b46d-b8fbbbdd129f.png)
  
> the credentials in the source code management is the privet key create with the public key added to the github repo
  
![image](https://user-images.githubusercontent.com/94615905/145450351-4dc0161a-9c43-4da7-a27b-159ee40dfa1a.png)


### creating  Dev branch and merge to main using jenkins

- create dev branch`git chechout -b dev`
 
![image](https://user-images.githubusercontent.com/94615905/145451635-2fa8b190-c30a-4072-afb9-4b528bfe3f4e.png)

 ![image](https://user-images.githubusercontent.com/94615905/145451716-8397952f-86ab-4c59-92e1-a65ce4d2f1c5.png)

 ![image](https://user-images.githubusercontent.com/94615905/145451833-34a86142-3d41-4853-bc6b-e4dfa01e24a0.png)


### using jenkins with aws ec2 instance
 
- create an ec2 instance on aws

#### jenkins

![image](https://user-images.githubusercontent.com/94615905/145452493-4c72c94e-8f6c-4367-871f-bc1f81fb0f2c.png)
  
![image](https://user-images.githubusercontent.com/94615905/145453226-806e877e-12a5-48c1-9f57-0a035e388783.png)
  
> Nothing selected for build triggers 
  
![image](https://user-images.githubusercontent.com/94615905/145452620-be8532e5-5dbe-4cc8-a1df-982e6c50ccb4.png)

> `jenkins(eng99)` is the eng99.pem file (key used when creating ec2 instance)
  

  
  
