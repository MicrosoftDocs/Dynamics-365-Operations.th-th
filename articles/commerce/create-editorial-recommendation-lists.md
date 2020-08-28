---
title: สร้างคำแนะนำที่ระบุด้วยตนเอง
description: หัวข้อนี้จะอธิบายวิธีการที่ผู้จัดซื้อสามารถสร้างและจัดการรายการผลิตภัณฑ์สำหรับลูกค้า Microsoft Dynamics 365 Commerce ได้ด้วยตนเอง
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 9826785700dcc1a35e6199b7aeff4e06b6d9da39
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665068"
---
# <a name="manually-create-curated-recommendations"></a><span data-ttu-id="03b79-103">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="03b79-103">Manually create curated recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03b79-104">หัวข้อนี้จะอธิบายวิธีการที่ผู้จัดซื้อสามารถสร้างและจัดการรายการคำแนะนำผลิตภัณฑ์สำหรับลูกค้า Microsoft Dynamics 365 Commerce ได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="03b79-104">This topic explains how merchandizers can manually create and manage product recommendations lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="03b79-105">รายการที่อนุรักษ์คือคอลเลกชันของเนื้อหาแต่ละรายการที่สร้างและอนุรักษ์โดยบุคคล</span><span class="sxs-lookup"><span data-stu-id="03b79-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="03b79-106">สร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="03b79-106">Create a new list</span></span>

<span data-ttu-id="03b79-107">เมื่อต้องการสร้างรายการแนะนำผลิตภัณฑ์ที่รวบรวมไว้ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="03b79-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="03b79-108">ไปยัง **Retail และ Commerce &gt; คำแนะนำผลิตภัณฑ์ &gt; รายการคำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="03b79-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="03b79-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="03b79-109">Select **New**.</span></span>
1. <span data-ttu-id="03b79-110">ในฟิลด์ **รหัสรายการ** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="03b79-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="03b79-111">ในฟิลด์ **ชื่อรายการ** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="03b79-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="03b79-112">**ชื่อรายการ** คือชื่อเรื่องของรายการที่จะปรากฏในส่วนรายการที่รวบรวมของโมดูล **การรวบรวมผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="03b79-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="03b79-113">ในการเพิ่มผลิตภัณฑ์ไปยังรายการ ให้เลือก **เพิ่มผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="03b79-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="03b79-114">เมื่อต้องการเปลี่ยนลำดับของผลิตภัณฑ์ในรายการ ให้ป้อนค่าในคอลัมน์ **ใบสั่งที่แสดง**</span><span class="sxs-lookup"><span data-stu-id="03b79-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="03b79-115">ถ้าผลิตภัณฑ์สองตัวมีมูลค่าของใบสั่งแสดงผลเดียวกัน ใบสั่งสุดท้ายของผลสองอย่างอาจแตกต่างจากฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="03b79-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="03b79-116">เลือก **บันทึก** เพื่อบันทึกรายการ</span><span class="sxs-lookup"><span data-stu-id="03b79-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="03b79-117">รายการตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="03b79-117">Example List</span></span>

![รายการการรวบรวมตัวอย่างในฝ่ายสนับสนุน](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="03b79-119">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="03b79-119">Additional resources</span></span>

[<span data-ttu-id="03b79-120">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="03b79-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="03b79-121">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="03b79-121">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="03b79-122">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="03b79-122">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="03b79-123">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="03b79-123">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="03b79-124">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="03b79-124">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="03b79-125">เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"</span><span class="sxs-lookup"><span data-stu-id="03b79-125">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="03b79-126">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="03b79-126">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="03b79-127">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="03b79-127">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="03b79-128">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="03b79-128">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="03b79-129">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="03b79-129">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="03b79-130">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="03b79-130">Product recommendations FAQ</span></span>](faq-recommendations.md)
