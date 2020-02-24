---
title: สร้างรายการคำแนะนำผลิตภัณฑ์ที่ระบุ
description: หัวข้อนี้จะอธิบายวิธีการที่ผู้จัดซื้อสามารถสร้างและจัดการรายการผลิตภัณฑ์สำหรับลูกค้า Microsoft Dynamics 365 Commerce ด้วยตนเอง
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 46fbd2d8c1235a6cb22c9341bcc21ee3754c8ede
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024944"
---
# <a name="create-curated-product-recommendation-lists"></a><span data-ttu-id="9ea32-103">สร้างรายการคำแนะนำผลิตภัณฑ์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="9ea32-103">Create curated product recommendation lists</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9ea32-104">หัวข้อนี้จะอธิบายวิธีการที่ผู้จัดซื้อสามารถสร้างและจัดการรายการผลิตภัณฑ์สำหรับลูกค้า Microsoft Dynamics 365 Commerce ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9ea32-104">This topic explains how merchandizers can create and manage manual product lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="9ea32-105">รายการที่อนุรักษ์คือคอลเลกชันของเนื้อหาแต่ละรายการที่สร้างและอนุรักษ์โดยบุคคล</span><span class="sxs-lookup"><span data-stu-id="9ea32-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="9ea32-106">สร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="9ea32-106">Create a new list</span></span>

<span data-ttu-id="9ea32-107">เมื่อต้องการสร้างรายการแนะนำผลิตภัณฑ์ที่รวบรวมไว้ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9ea32-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="9ea32-108">ไปยัง **Retail และ Commerce &gt; คำแนะนำผลิตภัณฑ์ &gt; รายการคำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="9ea32-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="9ea32-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="9ea32-109">Select **New**.</span></span>
1. <span data-ttu-id="9ea32-110">ในฟิลด์ **รหัสรายการ** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="9ea32-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="9ea32-111">ในฟิลด์ **ชื่อรายการ** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="9ea32-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="9ea32-112">**ชื่อรายการ** คือชื่อเรื่องของรายการที่จะปรากฏในส่วนรายการที่รวบรวมของโมดูล **การรวบรวมผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="9ea32-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="9ea32-113">ในการเพิ่มผลิตภัณฑ์ไปยังรายการ ให้เลือก **เพิ่มผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="9ea32-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="9ea32-114">เมื่อต้องการเปลี่ยนลำดับของผลิตภัณฑ์ในรายการ ให้ป้อนค่าในคอลัมน์ **ใบสั่งที่แสดง**</span><span class="sxs-lookup"><span data-stu-id="9ea32-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="9ea32-115">ถ้าผลิตภัณฑ์สองตัวมีมูลค่าของใบสั่งแสดงผลเดียวกัน ใบสั่งสุดท้ายของผลสองอย่างอาจแตกต่างจากฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="9ea32-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="9ea32-116">เลือก **บันทึก** เพื่อบันทึกรายการ</span><span class="sxs-lookup"><span data-stu-id="9ea32-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="9ea32-117">รายการตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="9ea32-117">Example List</span></span>

![รายการการรวบรวมตัวอย่างในฝ่ายสนับสนุน](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="9ea32-119">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9ea32-119">Additional resources</span></span>

[<span data-ttu-id="9ea32-120">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9ea32-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9ea32-121">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9ea32-121">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9ea32-122">เพิ่มรายการคำแนะนำผลิตภัณฑ์ลงในหน้า</span><span class="sxs-lookup"><span data-stu-id="9ea32-122">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="9ea32-123">ภาพรวมโมดูลการรวบรวมผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9ea32-123">Product collection module overview</span></span>](product-collection-module-overview.md)
