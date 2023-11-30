# Azure VPN cost saver
deletes and restores VPN gateways and connections to cut costs

These ARM templates create a storage account and 2 logic apps. The first logic runs at a specified time everyday and exports an ARM template for a VPN gateway and a connection object and saves them to the storage accout. It then deletes those resources. The second logic app also runs at a specified time everyday and restores the template from the storage account, re-creating the VPN gateway and connection. This can be useful for cost savings if the VPN only needs to exist during certain times. There is a template for an active/passive gateway with 1 connection and another template for an active/active gateway with 2 connections. If necessary more connections can be added manually to the logic apps after it is deployed.

Deploy for active/passive with 1 connection:
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fquiveringbacon%2FAzureVPNcostsaver%2Fmain%2Ftemplate%2520-%25201%2520connection.json)



Deploy for active/active with 2 connections:
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fquiveringbacon%2FAzureVPNcostsaver%2Fmain%2Ftemplate-multiconnection.json)
