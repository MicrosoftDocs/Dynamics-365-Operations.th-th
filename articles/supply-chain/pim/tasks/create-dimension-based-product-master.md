---
title: สร้างผลิตภัณฑ์หลักที่ใช้มิติ
description: 'ขั้นตอนนี้แสดงวิธีการสร้างผลิตภัณฑ์หลักใหม่ด้วยเทคโนโลยีการจัดโครงแบบตามมิติ '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductMasterDraftFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c3913bdf574036ed30f99701bf2b64ed0f713b1d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226086"
---
# <a name="create-a-dimension-based-product-master"></a><span data-ttu-id="8be84-103">สร้างผลิตภัณฑ์หลักที่ใช้มิติ</span><span class="sxs-lookup"><span data-stu-id="8be84-103">Create a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8be84-104">ขั้นตอนนี้แสดงวิธีการสร้างผลิตภัณฑ์หลักใหม่ด้วยเทคโนโลยีการจัดโครงแบบตามมิติ </span><span class="sxs-lookup"><span data-stu-id="8be84-104">This procedure shows how to create a new product master with dimension-based configuration technology.</span></span> <span data-ttu-id="8be84-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="8be84-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8be84-106">นี่เป็นกระบวนงานแรกจากแปดกระบวนงาน ที่อธิบายวิธีการสร้างชุดสำหรับการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="8be84-106">This is the first procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="8be84-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์หลัก </span><span class="sxs-lookup"><span data-stu-id="8be84-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="8be84-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="8be84-108">Click New.</span></span>
3. <span data-ttu-id="8be84-109">ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8be84-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="8be84-110">การป้อนหมายเลขผลิตภัณฑ์เป็นข้อบังคับ หากไม่ได้มีการตั้งค่าลำดับหมายเลขสำหรับฟิลด์หมายเลขผลิตภัณฑ์ไว้</span><span class="sxs-lookup"><span data-stu-id="8be84-110">Entering a product number is mandatory if no number sequence has been set up for the product number field.</span></span>  
4. <span data-ttu-id="8be84-111">ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="8be84-111">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="8be84-112">ในฟิลด์กลุ่มมิติของผลิตภัณฑ์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8be84-112">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8be84-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8be84-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8be84-114">เลือกมิติของการตั้งค่าคอนฟิกสำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="8be84-114">Select the configuration dimension for this procedure.</span></span>  
7. <span data-ttu-id="8be84-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8be84-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8be84-116">ในฟิลด์เทคโนโลยีการตั้งค่าคอนฟิก ให้เลือกตัวเลือก </span><span class="sxs-lookup"><span data-stu-id="8be84-116">In the Configuration technology field, select an option.</span></span>
    * <span data-ttu-id="8be84-117">เลือกเทคโนโลยีการตั้งค่าคอนฟิกตามมิติ</span><span class="sxs-lookup"><span data-stu-id="8be84-117">Select the Dimension-based configuration technology.</span></span>  
9. <span data-ttu-id="8be84-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8be84-118">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]