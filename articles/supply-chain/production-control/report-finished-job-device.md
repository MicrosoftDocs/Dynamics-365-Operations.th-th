---
title: รายงานเมื่อเสร็จไปยังสถานที่ที่ควบคุมป้ายทะเบียนจากอุปกรณ์สำหรับบัตรงาน
description: หัวข้อนี้อธิบายกระบวนการสำหรับการดำเนินการผลิตภัณฑ์สำเร็จรูปในใบสั่งผลิตไปยังสินค้าคงคลังเมื่อป้ายทะเบียนควบคุมที่ตั้ง
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 63073035941cd2ef343c65364536fe76a9b71430
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935133"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="2f150-103">รายงานเมื่อเสร็จไปยังสถานที่ที่ควบคุมป้ายทะเบียนจากอุปกรณ์สำหรับบัตรงาน</span><span class="sxs-lookup"><span data-stu-id="2f150-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="2f150-104">กระบวนการที่เรียกว่ารายงานเมื่อผลิตภัณฑ์สำเร็จรูปในใบสั่งผลิตเสร็จสมบูรณ์จนส่งไปยังสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2f150-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="2f150-105">ถ้าผลิตภัณฑ์สำเร็จรูปถูกเปิดใช้งานสำหรับกระบวนการคลังสินค้าขั้นสูง ผลิตภัณฑ์จะถูกรายงานว่าสำเร็จไปยังสถานที่ที่เรียกว่าที่สถานที่ผลิตผลผลิต</span><span class="sxs-lookup"><span data-stu-id="2f150-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="2f150-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าสถานที่ผลิตผลผลิต กรุณาดูที่ [สถานที่ผลิตผลผลิต](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)</span><span class="sxs-lookup"><span data-stu-id="2f150-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="2f150-107">ถ้าที่ตั้งเอาท์พุทการผลิตเป็นป้ายทะเบียนที่ควบคุม ต้องมีการระบุป้ายทะเบียนเมื่อมีการรายงานเป็นเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="2f150-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="2f150-108">ฟิลด์ **ป้ายทะเบียน** จะปรากฏทันทีบน **รายงานความคืบหน้า** บนหน้า **อุปกรณ์สำหรับบัตรงาน**</span><span class="sxs-lookup"><span data-stu-id="2f150-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="2f150-109">ฟิลด์จะปรากฏเฉพาะในพร้อมต์ **ความคืบหน้าของรายงาน** เมื่อรายงานเกี่ยวกับการดำเนินงานสุดท้ายของใบสั่งผลิตและสินค้าสำหรับใบสั่งผลิตถูกเปิดใช้งานสำหรับกระบวนการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="2f150-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="2f150-110">มีตัวเลือกสองตัวเลือกสำหรับการให้ป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="2f150-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="2f150-111">ผู้ใช้กำลังเลือกป้ายทะเบียนที่มีอยู่ในฟิลด์ป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="2f150-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="2f150-112">ป้ายทะเบียนจะถูกสร้างขึ้นโดยอัตโนมัติจากลำดับหมายเลขและถูกกำหนดเป็นค่าเริ่มต้นไปยังฟิลด์ป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="2f150-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="2f150-113">ตัวเลือกที่มีป้ายทะเบียนที่สร้างขึ้นโดยอัตโนมัติถูกตั้งค่าคอนฟิกโดยการเลือกตัวเลือก **สร้างป้ายทะเบียน** บนหน้า **ตั้งค่าคอนฟิกบัตรงานสำหรับอุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="2f150-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
