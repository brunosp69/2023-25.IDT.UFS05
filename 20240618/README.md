# App Service with Terraform

Following the official how to

https://learn.microsoft.com/en-us/azure/app-service/provision-resource-terraform


export TF_VAR_AZURE_RESOURCE_GROUP=learn-a0071223-a94d-40bc-9490-dbc44823466e
export TF_VAR_AZURE_APP_SERVICE_REPO_URL='https://github.com/brunosp69/2023-25.IDT.UFS05'

terraform init

terraform import azurerm_resource_group.rg 'learn-a0071223-a94d-40bc-9490-dbc44823466e'

az webapp log tail --name '...' --resource-group $TF_VAR_AZURE_RESOURCE_GROUP


node-red-dashboard

terraform destroy --target azurerm_linux_web_app.python_webapp

az login --use-device-code

-controlla se le subscription sono uguali
terraform init
importare AZURE_APP_SERVICE_REPO_URL e AZURE_RESOURCE_GROUP:

export TF_VAR_AZURE_APP_SERVICE_REPO_URL=
export TF_VAR_AZURE_RESOURCE_GROUP=''

per verificare: 

 echo $TF_VAR_AZURE_RESOURCE_GROUP
 
echo $TF_VAR_AZURE_APP_SERVICE_REPO_URL
terraform apply

se da errore e ti dice che la risorsa c’è già

terraform import azurerm_resource_group.rg '/subscriptions/id_subscrition/resourceGroups/id_reasurce_group’
terraform import azurerm_resource_group.rg ''

il link puoi copiarlo dall’errore
fai apply
NB poverata region:
riga 37 cambia region metti ‘eastus’
ovunque viene usato  azurerm_resource_group.rg.location
metti var.AZURE_REGION
riga 25 metti ‘eastus’ metti come valore di default

vai sul db del portale azure
aprire il firewall da network >add address
aggiungi un nuovo db su mysql connection
user:
psqladmin
password:
H@Sh1CoR3!


provisioring nodered
nella cartella 20240506 copia il contenuto di mqtt-poc.flow.json
importa sul file 