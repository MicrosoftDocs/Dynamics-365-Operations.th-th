---
title: ส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ
description: หัวข้อนี้อธิบายถึงฟังก์ชันที่จะช่วยให้สามารถส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบใน Microsoft Dynamics 365 for Retail
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
ms.openlocfilehash: c201311028b11121d626e93859a2b98497c047d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565311"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="c0ad7-103">ส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ</span><span class="sxs-lookup"><span data-stu-id="c0ad7-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="c0ad7-104">ใน Dynamics 365 for Finance and Operations รุ่น 10.0 การส่งคืนสินค้าสามารถดำเนินการกับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ ขณะที่รุ่นที่นำออกใช้ก่อนรุ่น 10.0 การส่งคืนสินค้าสามารถดำเนินการกับใบแจ้งหนี้ได้ครั้งละหนึ่งใบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c0ad7-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="c0ad7-105">ตั้งค่าคอนฟิก Retail ให้รองรับการส่งคืนสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ</span><span class="sxs-lookup"><span data-stu-id="c0ad7-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="c0ad7-106">ไปที่ **พารามิเตอร์ Retail \> ใบสั่งของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="c0ad7-107">เปิดพารามิเตอร์ **เปิดใช้งานการส่งคืนสำหรับใบสั่งหลายใบ**</span><span class="sxs-lookup"><span data-stu-id="c0ad7-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="c0ad7-108">ดำเนินการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="c0ad7-108">Process returns</span></span>

<span data-ttu-id="c0ad7-109">หลังจากเปิดพารามิเตอร์และทำข้อมูลการเปลี่ยนแปลงให้ตรงกับร้านค้า แคชเชียร์ในร้านค้าสามารถเลือกใบสั่งขายหลายใบของลูกค้าสำหรับการส่งคืนสินค้าของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="c0ad7-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="c0ad7-110">เมื่อเลือกใบสั่งแล้ว รายการของผลิตภัณฑ์ที่สามารถส่งคืนทั้งหมดในใบแจ้งหนี้ทั้งหมดสำหรับใบสั่งนั้นจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="c0ad7-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="c0ad7-111">แคชเชียร์สามารถเลือกผลิตภัณฑ์ที่จะส่งคืนได้</span><span class="sxs-lookup"><span data-stu-id="c0ad7-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="c0ad7-112">โดยจะมีการสร้างใบสั่งส่งคืนสินค้าใบเดียวสำหรับผลิตภัณฑ์ที่เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c0ad7-112">A single return order will be created for all the selected products.</span></span>
