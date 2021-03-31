---
title: สร้างคำแนะนำที่ระบุด้วยตนเอง
description: หัวข้อนี้จะอธิบายวิธีการที่ผู้จัดจำหน่ายสามารถสร้างและจัดการรายการผลิตภัณฑ์สำหรับลูกค้าด้วยตนเองสำหรับลูกค้า Microsoft Dynamics 365 Commerce
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7dd9de055a020d7171aa2dea45714933b0987d49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207998"
---
# <a name="manually-create-curated-recommendations"></a><span data-ttu-id="75e4f-103">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="75e4f-103">Manually create curated recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="75e4f-104">หัวข้อนี้จะอธิบายวิธีการที่ผู้จัดจำหน่ายสามารถสร้างและจัดการรายการผลิตภัณฑ์สำหรับลูกค้าด้วยตนเองสำหรับลูกค้า Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="75e4f-104">This topic explains how merchandizers can manually create and manage product recommendations lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="75e4f-105">รายการที่อนุรักษ์คือคอลเลกชันของเนื้อหาแต่ละรายการที่สร้างและอนุรักษ์โดยบุคคล</span><span class="sxs-lookup"><span data-stu-id="75e4f-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="75e4f-106">สร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="75e4f-106">Create a new list</span></span>

<span data-ttu-id="75e4f-107">เมื่อต้องการสร้างรายการแนะนำผลิตภัณฑ์ที่รวบรวมไว้ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="75e4f-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="75e4f-108">ไปยัง **Retail และ Commerce &gt; คำแนะนำผลิตภัณฑ์ &gt; รายการคำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="75e4f-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="75e4f-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="75e4f-109">Select **New**.</span></span>
1. <span data-ttu-id="75e4f-110">ในฟิลด์ **รหัสรายการ** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="75e4f-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="75e4f-111">ในฟิลด์ **ชื่อรายการ** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="75e4f-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="75e4f-112">**ชื่อรายการ** คือชื่อเรื่องของรายการที่จะปรากฏในส่วนรายการที่รวบรวมของโมดูล **การรวบรวมผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="75e4f-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="75e4f-113">ในการเพิ่มผลิตภัณฑ์ไปยังรายการ ให้เลือก **เพิ่มผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="75e4f-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="75e4f-114">เมื่อต้องการเปลี่ยนลำดับของผลิตภัณฑ์ในรายการ ให้ป้อนค่าในคอลัมน์ **ใบสั่งที่แสดง**</span><span class="sxs-lookup"><span data-stu-id="75e4f-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="75e4f-115">ถ้าผลิตภัณฑ์สองตัวมีมูลค่าของใบสั่งแสดงผลเดียวกัน ใบสั่งสุดท้ายของผลสองอย่างอาจแตกต่างจากฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="75e4f-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="75e4f-116">เลือก **บันทึก** เพื่อบันทึกรายการ</span><span class="sxs-lookup"><span data-stu-id="75e4f-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="75e4f-117">รายการตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="75e4f-117">Example List</span></span>

![รายการการรวบรวมตัวอย่างในฝ่ายสนับสนุน](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="75e4f-119">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="75e4f-119">Additional resources</span></span>

[<span data-ttu-id="75e4f-120">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="75e4f-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="75e4f-121">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="75e4f-121">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="75e4f-122">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="75e4f-122">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="75e4f-123">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="75e4f-123">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="75e4f-124">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="75e4f-124">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="75e4f-125">เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"</span><span class="sxs-lookup"><span data-stu-id="75e4f-125">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="75e4f-126">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="75e4f-126">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="75e4f-127">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="75e4f-127">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="75e4f-128">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="75e4f-128">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="75e4f-129">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="75e4f-129">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="75e4f-130">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="75e4f-130">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]