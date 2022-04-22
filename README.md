# learn-terraform-azure
Building infrastructure in Azure
<p> To start building infrastructure in Azure, you need to first have an Azure subscription</p>
<p><ol>
  <li> Login into the Azure CLI <b><i>az login</b></i>....The browser will prompt you for your Azure login</li>
  <li> Once you are logged in, the terminal will show you all your subscriptions. Make sure to copy the <b>"id"</b> from the subscription that you want to use</li>
  <li> Set the account by running <b>az account set --subscription "subscription-id"</b></li>
  <li> Create a Contributor role under the subscription using:
    <br><b>az ad sp create-for-rbac --role="Contributor" --scopes="/subscriptions/SUBSCRIPTION_ID"</b></br>
    <p><b><i>Note</i></b>: The output will show you information that must only be for your use so save it somewhere safe!</p></li>
  <li> Now in PowerShell, you can set the environment variable that you saved from the previous command.
      <br> $ $Env:ARM_CLIENT_ID = "APPID_VALUE"</br>
      <br>$ $Env:ARM_CLIENT_SECRET = "PASSWORD_VALUE"</br>
      <br>$ $Env:ARM_SUBSCRIPTION_ID = "SUBSCRIPTION_ID"</br>
      <br>$ $Env:ARM_TENANT_ID = "TENANT_VALUE"</br></li>
   <li> You can create a new directory in PowerShell called <b>"terraform-azure"</b> using the command:
  <br><b>New-Item -Path "c:\" -Name "terraform-azure" -ItemType "directory"</b></br></li>
  <li>Create a new file in VS code called <b>"main.tf"</b> An example is listed in this repository.
<br>Make sure to update the region to the one that you are using in Azure</br></li>
