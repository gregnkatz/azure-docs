---
title: What are Azure Reservations?
description: Learn about Azure Reservations and pricing to save on your virtual machines, SQL databases, Azure Cosmos DB, and other resource costs.
author: yashesvi
ms.reviewer: yashar
ms.service: cost-management-billing
ms.topic: conceptual
ms.date: 03/30/2020
ms.author: banders
---

# What are Azure Reservations?

Azure Reservations help you save money by committing to one-year or three-years plans for multiple products. Committing allows you to get a discount on the resources you use. Reservations can significantly reduce your resource costs up to 72% on pay-as-you-go prices. Reservations provide a billing discount and don't affect the runtime state of your resources. After you purchase a reservation, the discount automatically applies to matching resources.

You can pay for a reservation up front or monthly. The total cost of up-front and monthly reservations is the same and you don't pay any extra fees when you choose to pay monthly. Monthly payment is available for Azure reservations, not third-party products.

You can buy a reservation in the Azure portal at [https://portal.azure.com/#blade/Microsoft_Azure_Reservations/ReservationsBrowseBlade](https://portal.azure.com/#blade/Microsoft_Azure_Reservations/ReservationsBrowseBlade).

## Why buy a reservation?

If you have consistent resource usage that supports reservations, buying a reservation gives you the option to reduce your costs. For example, when you continuously run instances of a service without a reservation, you're charged at pay-as-you-go rates. When you buy a reservation, you immediately get the reservation discount. The resources are no longer charged at the pay-as-you-go rates.

## How reservation discount is applied

After purchase, the reservation discount automatically applies to the resource usage that matches the attributes you select when you buy the reservation. Attributes include the SKU, regions (where applicable), and scope. Reservation scope selects where the reservation savings apply.

For more information about how discount is applied, see [Reserved instance discount application](reservation-discount-application.md).

For more information about how reservation scope works, see [Scope reservations](prepare-buy-reservation.md#scope-reservations).

## Determine what to purchase 

All reservations, except Azure Databricks, are applied on an hourly basis. Consider reservation purchases based on your consistent base usage. You can determine which reservation to purchase by analyzing your usage data or by using reservation recommendations. Recommendations are available in:

- Azure advisor (VMs only)
- Reservation purchase experience in the Azure portal
- Cost Management Power BI app
- APIs 

For more information, see [Determine what reservation to purchase](determine-reservation-purchase.md) 

## Buying a reservation 

You can purchase reservations from the Azure portal, APIs, PowerShell, and CLI. 

Go to Azure portal to purchase (https://ms.portal.azure.com/#blade/Microsoft_Azure_Reservations/CreateBlade/referrer/Docs) 

For more information, see [Buy a reservation](prepare-buy-reservation.md) 

## How is a reservation billed? 

The reservation is charged to the payment method tied to the subscription. The reservation cost is deducted from your monetary commitment balance, if available. When your monetary commitment balance doesn't cover the cost of the reservation, you're billed the overage. If you have a subscription from an individual plan with pay-as-you-go rates, the credit card you have on your account is billed immediately for up-front purchases. Monthly payments appear on your invoice and your credit card is charged monthly. When you're billed by invoice, you see the charges on your next invoice. 

## Permissions to view and manage reservations 

The user who purchases a reservation and the account administrator of the subscription used for billing the reservation get the Owner role on the reservation order and the reservation.

You can delegate reservation management by adding people to roles on the reservation order or the reservation. You assign the roles in the Azure portal or by using APIs and PowerShell. 

For more information, see [Add or change users who can manage a reservation](manage-reserved-vm-instance.md#add-or-change-users-who-can-manage-a-reservation) 

## Get reservation details and utilization after purchase

If you have permission to view to the reservation, you can see it and its use in the Azure portal. You can get the data using APIs, as well. 

For more information on how to see reservations in Azure portal, see [View reservations in the Azure portal](view-reservations.md) 

## Manage reservations after purchase 

After you buy an Azure reservation, you can update the scope to apply reservation to a different subscription, change who can manage the reservation, split a reservation into smaller parts, or change instance size flexibility. 

For more information, see [Manage Reservations for Azure resources](manage-reserved-vm-instance.md) 

## Flexibility with Azure reservations

Azure Reservations provide flexibility to help meet your evolving needs. You can exchange a reservation for another reservation of the same type. You can also refund a reservation, up to $50,000 USD in a 12 month rolling window, if you no longer need it. The maximum limit of the refund applies to all reservations in the scope of your agreement with Microsoft.

For more information, see [Self-service exchanges and refunds for Azure Reservations](exchange-and-refund-azure-reservations.md)


## Charges covered by reservation

- **Reserved Virtual Machine Instance** - A reservation only covers the virtual machine compute costs. It doesn't cover additional software, Windows, networking, or storage charges.
- **Azure Storage reserved capacity** - A reservation covers storage capacity for standard storage accounts for Blob storage or Azure Data Lake Gen2 storage. The reservation doesn't cover bandwidth or transaction rates.
- **Azure Cosmos DB reserved capacity** - A reservation covers throughput provisioned for your resources. It doesn't cover the storage and networking charges.
- **SQL Database reserved vCore** - Only the compute costs are included with a reservation. The SQL license is billed separately.
- **SQL Data Warehouse** - A reservation covers cDWU usage. It doesn't cover storage or networking charges associated with the SQL Data Warehouse usage.
- **Azure Databricks** - A reservation covers only the DBU usage. Other charges, such as compute, storage, and networking, are applied separately.
- **App Service stamp fee** - A reservation covers stamp usage. It doesn't apply to workers, so any other resources associated with the stamp are charged separately.
- **Azure Database for MySQL** - Only the compute costs are included with a reservation. A reservation doesn't cover software, networking, or storage charges associated with the MySQL Database server.
- **Azure Database for PostgreSQL** - Only the compute costs are included with a reservation. A reservation doesn't cover software, networking, or storage charges associated with the PostgreSQL Database servers.
- **Azure Database for MariaDB** - Only the compute costs are included with a reservation. A reservation doesn't cover software, networking, or storage charges associated with the MariaDB Database server.
- **Azure Data Explorer** - A reservation covers the markup charges. A reservation doesn't apply to compute, networking, or storage charges associated with the clusters.
- **Azure Cache for Redis** - Only the compute costs are included with a reservation. A reservation doesn't cover networking or storage charges associated with the Redis cache instances.
- **Azure Dedicated Host** - Only the compute costs are included with the Dedicated host.
- **Azure Disk Storage reservations** - A reservation only covers premium SSDs of P30 size or greater. It doesn't cover any other disk types or sizes smaller than P30.

Software plans:

- **SUSE Linux** - A reservation covers the software plan costs. The discounts apply only to SUSE meters and not to the virtual machine usage.
- **Red Hat Plans** - A reservation covers the software plan costs. The discounts apply only to RedHat meters and not to the virtual machine usage.
- **Azure VMware Solution by CloudSimple** - A reservation covers the VMWare CloudSimple Nodes. Additional software costs still apply.
- **Azure Red Hat OpenShift** - A reservation applies to the OpenShift costs, not to Azure infrastructure costs.

For Windows virtual machines and SQL Database, the reservation discount doesn't apply to the software costs. You can cover the licensing costs with [Azure Hybrid Benefit](https://azure.microsoft.com/pricing/hybrid-benefit/).


## Need help? Contact us.

If you have questions or need help,  [create a support request](https://go.microsoft.com/fwlink/?linkid=2083458).

## Next steps

- Learn more about Azure Reservations with the following articles:
    - [Manage Azure Reservations](manage-reserved-vm-instance.md)
    - [Understand reservation usage for your subscription with pay-as-you-go rates](understand-reserved-instance-usage.md)
    - [Understand reservation usage for your Enterprise enrollment](understand-reserved-instance-usage-ea.md)
    - [Windows software costs not included with reservations](reserved-instance-windows-software-costs.md)
    - [Azure Reservations in Partner Center Cloud Solution Provider (CSP) program](/partner-center/azure-reservations)

- Learn more about reservations for service plans:
    - [Virtual Machines with Azure Reserved VM Instances](../../virtual-machines/windows/prepay-reserved-vm-instances.md)
    - [Azure Cosmos DB resources with Azure Cosmos DB reserved capacity](../../cosmos-db/cosmos-db-reserved-capacity.md)
    - [SQL Database compute resources with Azure SQL Database reserved capacity](../../sql-database/sql-database-reserved-capacity.md)
Learn more about reservations for software plans:
    - [Red Hat software plans from Azure Reservations](../../virtual-machines/linux/prepay-rhel-software-charges.md)
    - [SUSE software plans from Azure Reservations](../../virtual-machines/linux/prepay-suse-software-charges.md)
