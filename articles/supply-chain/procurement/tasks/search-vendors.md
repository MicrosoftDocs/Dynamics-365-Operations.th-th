---
title: ค้นหาผู้จัดจำหน่าย
description: 'เรียนรู้วิธีการค้นหาผู้จัดจำหน่ายตามเงื่อนไขที่ระบุ '
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 494f28ad6cf6f973b090a5d0f745eb530256925c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811929"
---
# <a name="search-for-vendors"></a><span data-ttu-id="2376e-103">ค้นหาผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2376e-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2376e-104">เรียนรู้วิธีการค้นหาผู้จัดจำหน่ายตามเงื่อนไขที่ระบุ </span><span class="sxs-lookup"><span data-stu-id="2376e-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="2376e-105">ตัวอย่างนี้แสดงวิธีการค้นหาผู้จัดจำหน่ายที่ได้รับอนุมัติสำหรับประเภทการจัดซื้อเฉพาะ และมีที่อยู่หลักของพวกเขาในประเทศเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="2376e-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="2376e-106">คุณสามารถรันขั้นตอนนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="2376e-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="2376e-107">งานนี้อาจมักจะถูกดำเนินการโดยผู้เชี่ยวชาญด้านการจัดซื้อจัดหา</span><span class="sxs-lookup"><span data-stu-id="2376e-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="2376e-108">ไปที่การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > การค้นหาผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2376e-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="2376e-109">คลิกที่ไอคอนบวกเพื่อเปิดหน้าการเลือกประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="2376e-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="2376e-110">ในแผนภูมิ เลือก 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'</span><span class="sxs-lookup"><span data-stu-id="2376e-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="2376e-111">ถ้าคุณกำลังใช้งานขั้นตอนนี้เป็นคู่มืองาน คุณอาจจะต้องคลิกปุ่มปลดล็อกก่อนที่จะเลือกโหนดที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2376e-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="2376e-112">ถ้าคุณไม่ได้ใช้ USMF เลือกหนึ่งในประเภทที่คุณมี</span><span class="sxs-lookup"><span data-stu-id="2376e-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="2376e-113">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="2376e-113">Click Add.</span></span>
    * <span data-ttu-id="2376e-114">สามารถเลือกมากกว่าหนึ่งประเภทที่นี่</span><span class="sxs-lookup"><span data-stu-id="2376e-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="2376e-115">ถ้าคุณทำเช่นนั้น การค้นหาจะค้นหาผู้จัดจำหน่ายที่ได้รับการอนุมัติอย่างน้อยหนึ่งประเภท</span><span class="sxs-lookup"><span data-stu-id="2376e-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="2376e-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2376e-116">Click OK.</span></span>
6. <span data-ttu-id="2376e-117">ในฟิลด์ประเทศ/ภูมิภาค ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2376e-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="2376e-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2376e-118">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]