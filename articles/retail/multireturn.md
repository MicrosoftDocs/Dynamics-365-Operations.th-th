---
title: ส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ
description: หัวข้อนี้อธิบายถึงฟังก์ชันที่จะช่วยให้สามารถส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบใน Dynamics 365 Retail
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018000"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="8691e-103">ส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ</span><span class="sxs-lookup"><span data-stu-id="8691e-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="8691e-104">การส่งคืนสินค้าสามารถดำเนินการกับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ</span><span class="sxs-lookup"><span data-stu-id="8691e-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="8691e-105">ตั้งค่าคอนฟิก Retail ให้รองรับการส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ</span><span class="sxs-lookup"><span data-stu-id="8691e-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="8691e-106">ไปที่ **พารามิเตอร์ Retail \> ใบสั่งของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="8691e-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="8691e-107">เปิดพารามิเตอร์ **เปิดใช้งานการส่งคืนสำหรับใบสั่งหลายใบ**</span><span class="sxs-lookup"><span data-stu-id="8691e-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="8691e-108">ดำเนินการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="8691e-108">Process returns</span></span>

<span data-ttu-id="8691e-109">หลังจากเปิดพารามิเตอร์และทำข้อมูลการเปลี่ยนแปลงให้ตรงกับร้านค้า แคชเชียร์ในร้านค้าสามารถเลือกใบสั่งขายหลายใบของลูกค้าสำหรับการส่งคืนสินค้าของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="8691e-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="8691e-110">เมื่อเลือกใบสั่งแล้ว รายการของผลิตภัณฑ์ที่สามารถส่งคืนทั้งหมดในใบแจ้งหนี้ทั้งหมดสำหรับใบสั่งนั้นจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8691e-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="8691e-111">แคชเชียร์สามารถเลือกผลิตภัณฑ์ที่จะส่งคืนได้</span><span class="sxs-lookup"><span data-stu-id="8691e-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="8691e-112">โดยจะมีการสร้างใบสั่งส่งคืนสินค้าใบเดียวสำหรับผลิตภัณฑ์ที่เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8691e-112">A single return order will be created for all the selected products.</span></span>
