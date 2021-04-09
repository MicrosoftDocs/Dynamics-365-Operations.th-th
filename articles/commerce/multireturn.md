---
title: ส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ
description: หัวข้อนี้อธิบายถึงฟังก์ชันที่จะช่วยให้สามารถส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบใน Dynamics 365 Commerce
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4a64794a0e04516441fab628d441640e4d154b8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796908"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="cbca0-103">ส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ</span><span class="sxs-lookup"><span data-stu-id="cbca0-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="cbca0-104">บทความนี้อธิบายถึงคุณลักษณะสองชนิดที่จะเพิ่มประสิทธิภาพการส่งคืนใบแจ้งหนี้ของลูกค้าสำหรับใบแจ้งหนี้หลายใบ</span><span class="sxs-lookup"><span data-stu-id="cbca0-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="cbca0-105">เปิดใช้งานการขอคืนเงินสำหรับการบันทึกหลายครั้ง</span><span class="sxs-lookup"><span data-stu-id="cbca0-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="cbca0-106">คุณลักษณะนี้จะเปิดใช้งานการขอคืนเงินที่มีการเชื่อมโยงหลายรายการกับใบสั่งของลูกค้ารายเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cbca0-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="cbca0-107">ไปที่พื้นที่ทำงาน **การจัดการคุณลักษณะ** และค้นหา **เปิดใช้งานการขอคืนเงินสำหรับการบันทึกหลายครั้ง**</span><span class="sxs-lookup"><span data-stu-id="cbca0-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="cbca0-108">เลือก **เปิดใช้งานการขอคืนเงินสำหรับใบสั่งหลายรายการ** จากนั้นคลิก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="cbca0-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="cbca0-109">เปิดใช้งานการคำนวณภาษีที่เหมาะสมสำหรับการส่งคืนพร้อมปริมาณบางส่วน</span><span class="sxs-lookup"><span data-stu-id="cbca0-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="cbca0-110">คุณลักษณะนี้จะช่วยตรวจสอบว่าเมื่อมีการส่งคืนใบสั่งงานโดยใช้ใบแจ้งหนี้หลายใบ ภาษีจะมียอดเท่ากับยอดภาษีที่เรียกเก็บในครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="cbca0-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="cbca0-111">ไปที่พื้นที่ทำงาน **การจัดการคุณลักษณะ** และค้นหา **เปิดใช้งานการคำนวณภาษีที่เหมาะสมสำหรับการส่งคืนพร้อมปริมาณบางส่วน**</span><span class="sxs-lookup"><span data-stu-id="cbca0-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="cbca0-112">เลือก **เปิดใช้งานการคำนวณภาษีที่เหมาะสมสำหรับการส่งคืนพร้อมปริมาณบางส่วน** จากนั้นคลิก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="cbca0-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="cbca0-113">ดำเนินการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="cbca0-113">Process returns</span></span>

<span data-ttu-id="cbca0-114">หลังจากเปิดคุณลักษณะเหล่านี้และทำข้อมูลการเปลี่ยนแปลงให้ตรงกับร้านค้า แคชเชียร์ในร้านค้าสามารถเลือกใบสั่งขายหลายใบของลูกค้าสำหรับการส่งคืนสินค้าของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="cbca0-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="cbca0-115">เมื่อเลือกใบสั่งแล้ว รายการของผลิตภัณฑ์ที่สามารถส่งคืนทั้งหมดในใบแจ้งหนี้ทั้งหมดสำหรับใบสั่งนั้นจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="cbca0-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="cbca0-116">แคชเชียร์สามารถเลือกผลิตภัณฑ์ที่จะส่งคืนได้</span><span class="sxs-lookup"><span data-stu-id="cbca0-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="cbca0-117">โดยจะมีการสร้างใบสั่งส่งคืนสินค้าใบเดียวสำหรับผลิตภัณฑ์ที่เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cbca0-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="cbca0-118">หากมีการส่งคืนใบสั่งงานเต็มจำนวน ยอดภาษีที่คืนมาให้ลูกค้าจะเท่ากับยอดภาษีที่เรียกเก็บในครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="cbca0-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]