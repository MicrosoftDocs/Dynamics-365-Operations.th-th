---
title: ส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ
description: หัวข้อนี้อธิบายถึงฟังก์ชันที่จะช่วยให้สามารถส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบใน Dynamics 365 Commerce
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
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
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460012"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="53040-103">ส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ</span><span class="sxs-lookup"><span data-stu-id="53040-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="53040-104">บทความนี้อธิบายถึงคุณลักษณะสองชนิดที่จะเพิ่มประสิทธิภาพการส่งคืนใบแจ้งหนี้ของลูกค้าสำหรับใบแจ้งหนี้หลายใบ</span><span class="sxs-lookup"><span data-stu-id="53040-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="53040-105">เปิดใช้งานการขอคืนเงินสำหรับการบันทึกหลายครั้ง</span><span class="sxs-lookup"><span data-stu-id="53040-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="53040-106">คุณลักษณะนี้จะเปิดใช้งานการขอคืนเงินที่มีการเชื่อมโยงหลายรายการกับใบสั่งของลูกค้ารายเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="53040-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="53040-107">ไปที่พื้นที่ทำงาน **การจัดการคุณลักษณะ** และค้นหา **เปิดใช้งานการขอคืนเงินสำหรับการบันทึกหลายครั้ง**</span><span class="sxs-lookup"><span data-stu-id="53040-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="53040-108">เลือก **เปิดใช้งานการขอคืนเงินสำหรับใบสั่งหลายรายการ** จากนั้นคลิก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="53040-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="53040-109">เปิดใช้งานการคำนวณภาษีที่เหมาะสมสำหรับการส่งคืนพร้อมปริมาณบางส่วน</span><span class="sxs-lookup"><span data-stu-id="53040-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="53040-110">คุณลักษณะนี้จะช่วยตรวจสอบว่าเมื่อมีการส่งคืนใบสั่งงานโดยใช้ใบแจ้งหนี้หลายใบ ภาษีจะมียอดเท่ากับยอดภาษีที่เรียกเก็บในครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="53040-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="53040-111">ไปที่พื้นที่ทำงาน **การจัดการคุณลักษณะ** และค้นหา **เปิดใช้งานการคำนวณภาษีที่เหมาะสมสำหรับการส่งคืนพร้อมปริมาณบางส่วน**</span><span class="sxs-lookup"><span data-stu-id="53040-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="53040-112">เลือก **เปิดใช้งานการคำนวณภาษีที่เหมาะสมสำหรับการส่งคืนพร้อมปริมาณบางส่วน** จากนั้นคลิก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="53040-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="53040-113">ดำเนินการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="53040-113">Process returns</span></span>

<span data-ttu-id="53040-114">หลังจากเปิดคุณลักษณะเหล่านี้และทำข้อมูลการเปลี่ยนแปลงให้ตรงกับร้านค้า แคชเชียร์ในร้านค้าสามารถเลือกใบสั่งขายหลายใบของลูกค้าสำหรับการส่งคืนสินค้าของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="53040-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="53040-115">เมื่อเลือกใบสั่งแล้ว รายการของผลิตภัณฑ์ที่สามารถส่งคืนทั้งหมดในใบแจ้งหนี้ทั้งหมดสำหรับใบสั่งนั้นจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="53040-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="53040-116">แคชเชียร์สามารถเลือกผลิตภัณฑ์ที่จะส่งคืนได้</span><span class="sxs-lookup"><span data-stu-id="53040-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="53040-117">โดยจะมีการสร้างใบสั่งส่งคืนสินค้าใบเดียวสำหรับผลิตภัณฑ์ที่เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="53040-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="53040-118">หากมีการส่งคืนใบสั่งงานเต็มจำนวน ยอดภาษีที่คืนมาให้ลูกค้าจะเท่ากับยอดภาษีที่เรียกเก็บในครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="53040-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>

