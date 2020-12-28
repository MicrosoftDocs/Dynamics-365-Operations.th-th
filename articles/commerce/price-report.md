---
title: รายงานราคาขายปลีก
description: หัวข้อนี้แสดงภาพรวมของลักษณะการทำงานของรายงานราคาที่ใช้เพื่อดูการเปลี่ยนแปลงราคาที่กำลังจะมาถึงสำหรับผลิตภัณฑ์ที่จัดประเภท
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 91c0a96abdd7df9e85e63ca6b1b47a57f3f401eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416004"
---
# <a name="retail-price-reports"></a><span data-ttu-id="4a1e4-103">รายงานราคาขายปลีก</span><span class="sxs-lookup"><span data-stu-id="4a1e4-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="4a1e4-104">เมื่อต้องการให้ราคาแข่งขันกับลูกค้า ผู้ค้าปลีกมักจะเปลี่ยนราคาของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4a1e4-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="4a1e4-105">ผู้จัดการร้านค้าต้องการความสามารถที่จะได้รับการเข้าถึงการเปลี่ยนแปลงราคาที่กำลังจะมาถึงได้อย่างง่ายดาย เพื่อให้พวกเขาสามารถวางแผนสำหรับทรัพยากรที่จำเป็นเพื่ออัพเดตป้ายราคาที่แสดงบนชั้นวางของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="4a1e4-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="4a1e4-106">ด้วยการเปิดตัวการขายปลีก 10.0 ผู้จัดการร้านค้าสามารถเปิดรายงาน **ราคา** โดยนำทางไปที่ **ทุกร้านค้า \> ร้านค้า \> รายงานราคา** และดูราคาปรับปรุงล่าสุดสำหรับผลิตภัณฑ์ที่เกี่ยวข้องกับร้านค้า </span><span class="sxs-lookup"><span data-stu-id="4a1e4-106">With release 10.0 of Retail, a store manager can open the **Price** report by navigating to **All stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="4a1e4-107">หากต้องการเปิดใช้งานรายงานราคา ต้องเปิดพารามิเตอร์ **เปิดใช้รายงานราคาสำหรับร้านค้า** </span><span class="sxs-lookup"><span data-stu-id="4a1e4-107">To enable the price report, the **Enable price report for store** parameter must be turned on.</span></span> <span data-ttu-id="4a1e4-108">พารามิเตอร์นี้ตั้งอยู่บนแท็บ **พารามิเตอร์การค้า \> ส่วนลด \> เบ็ดเตล็ด** เปิดหน้า **รายงานราคา** จะแสดงกล่องโต้ตอบพร้อมการกำหนดค่าต่างๆ</span><span class="sxs-lookup"><span data-stu-id="4a1e4-108">This parameter is located on the **Commerce parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="4a1e4-109">การตั้งค่าคอนฟิกที่พร้อมใช้งานมีแสดงรายการอยู่ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="4a1e4-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="4a1e4-110">โครงแบบ</span><span class="sxs-lookup"><span data-stu-id="4a1e4-110">Configuration</span></span> | <span data-ttu-id="4a1e4-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4a1e4-111">Description</span></span> |
|---|---|
| <span data-ttu-id="4a1e4-112">วันที่เริ่มต้น / วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="4a1e4-112">From date / To date</span></span>| <span data-ttu-id="4a1e4-113">ช่วงวันที่สำหรับรายงานราคาควรถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="4a1e4-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="4a1e4-114">ในขณะนี้ระยะเวลาถูกจำกัดที่ 7 วัน</span><span class="sxs-lookup"><span data-stu-id="4a1e4-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="4a1e4-115">ช่องสัญญาณ</span><span class="sxs-lookup"><span data-stu-id="4a1e4-115">Channel</span></span>| <span data-ttu-id="4a1e4-116">ร้านค้าที่ควรมีการสร้างรายงานราคา</span><span class="sxs-lookup"><span data-stu-id="4a1e4-116">The store for which the price report should be generated.</span></span> |
| <span data-ttu-id="4a1e4-117">แสดงผลิตภัณฑ์ที่มีสินค้าคงคลังที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4a1e4-117">Display products with available inventory</span></span>| <span data-ttu-id="4a1e4-118">การตั้งค่านี้เป็น **ใช่** จะแสดงราคาสำหรับเฉพาะผลิตภัณฑ์ที่ขณะนี้มีสินค้าคงคลังอยู่จริงในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="4a1e4-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="4a1e4-119">แสดงราคาสำหรับผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="4a1e4-119">Display prices for variants</span></span> | <span data-ttu-id="4a1e4-120">การตั้งค่านี้เป็น **ใช่** จะแสดงราคาของผลิตภัณฑ์ย่อยพร้อมกับผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="4a1e4-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="4a1e4-121">ตัวเลือกนี้ควรถูก **เปิด** เฉพาะเมื่อคุณมีราคาเฉพาะผลิตภัณฑ์ย่อย เนื่องจากจำนวนแถวจะเพิ่มขึ้นอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="4a1e4-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="4a1e4-122">ในการนำออกใช้ในอนาคต เราจะเปิดใช้งานราคาตามมิติเพื่อให้ผู้จัดการร้านค้าสามารถเลือกมิติที่ควรจะแสดงราคา</span><span class="sxs-lookup"><span data-stu-id="4a1e4-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="4a1e4-123">แสดงผลิตภัณฑ์ที่มีการเปลี่ยนแปลงราคา</span><span class="sxs-lookup"><span data-stu-id="4a1e4-123">Display products with price changes</span></span> | <span data-ttu-id="4a1e4-124">การตั้งค่านี้เป็น **ใช่** จะแสดงราคาสำหรับเฉพาะวันที่ที่มีการเปลี่ยนราคา</span><span class="sxs-lookup"><span data-stu-id="4a1e4-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="4a1e4-125">ราคาสำหรับ *หนึ่งวันก่อนหน้า* **วันที่เริ่มต้น** ที่เลือกไว้จะแสดงขึ้นเสมอ เพื่อให้ผู้จัดการร้านค้าสามารถระบุผลิตภัณฑ์ที่มีการเปลี่ยนแปลงราคาสำหรับระยะเวลาที่เลือกทั้งหมดได้ง่าย และยังสามารถดูราคาปัจจุบันได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="4a1e4-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="4a1e4-126">หลังจากที่มีการสร้างรายงาน คุณสามารถดาวน์โหลดไฟล์ Excel สำหรับความต้องการการกรองข้อมูลเพิ่มเติมใด ๆ</span><span class="sxs-lookup"><span data-stu-id="4a1e4-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="4a1e4-127">นอกจากนี้ยังสามารถใช้รายงานราคาเพื่อตรวจสอบราคาของผลิตภัณฑ์ในอดีตสำหรับวันที่ผ่านมาได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="4a1e4-127">The price report can also be used to check the historical prices of products for past dates.</span></span>
