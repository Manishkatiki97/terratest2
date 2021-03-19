# terratest2
## These files have the code to initate the EC2 and test it using terratest.

### **Steps**
- From the repository run the following commands using teraform to make sure the instance is working
    - `terraform init`
    - `terraform plan`
    - `terraform apply`
    - **Note**: Make sure the instance is created and there are no errors
    - `terraform destroy`
- Now create the git repository in the directory on the local file
- Push the changes to the github repository
- To configure dependencies, run: 
    - `go mod init <MODULE_NAME>`
- The following command runs the `terraform init`, `terraform apply`, checks the HTTP response and then runs `terraform destroy`
    - go test -v -run TestTerraformAWS - timeout 30m 
    - **Note**: Make sure all the necessary modules are installed 
- Resources: 
    - https://github.com/gruntwork-io/terratest/tree/master/modules
    - https://github.com/gruntwork-io/terratest/tree/master/examples/terraform-basic-example/
    - https://terratest.gruntwork.io/docs/getting-started/quick-start/
