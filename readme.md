# Azure Key Vault
Er en skystjenese som tilbyr en sikker lagring for secrets slik som: nøkler, passord, og sertifikater. 

Her viser vi hvordan man oppretter en `azurerm_key_vault`med bruk av Terraform.

## Initialiser Terraform
Kjør `terraform init`for å initialisere Terraform deployment. Denne kommandoen laster ned Azure provider som er nødvendig for å administrere Azure ressursene.

```hcl
terraform init -upgrade
```

## Lag en Terraform utførelsesplan
Kjør `terraform apply` for legge til utførelsesplanen til skyinfrastrukturen.

```hcl
terraform plan -out main.tfplan
```

## Rydd opp ressurser
1. Kjør `terraform plan` og spesifiser `destroy`flagget.

```hcl
terraform plan -destroy -out main.destroy.tfplan
```

2. Kjør `terraform apply` for legge til utførelsesplanen

```hcl
terraform apply main.destroy.tfplan
```
