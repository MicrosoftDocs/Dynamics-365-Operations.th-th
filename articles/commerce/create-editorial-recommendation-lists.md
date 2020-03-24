---
title: สร้างคำแนะนำที่ระบุด้วยตนเอง
description: หัวข้อนี้จะอธิบายวิธีการที่ผู้จัดซื้อสามารถสร้างและจัดการรายการผลิตภัณฑ์สำหรับลูกค้า Microsoft Dynamics 365 Commerce ได้ด้วยตนเอง
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: b39ef61e7dabdd8a53d5666926a95cb7b9e6b9a5
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127732"
---
# <a name="manually-create-curated-recommendations"></a><span data-ttu-id="b83cb-103">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b83cb-103">Manually create curated recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b83cb-104">หัวข้อนี้จะอธิบายวิธีการที่ผู้จัดซื้อสามารถสร้างและจัดการรายการคำแนะนำผลิตภัณฑ์สำหรับลูกค้า Microsoft Dynamics 365 Commerce ได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b83cb-104">This topic explains how merchandizers can manually create and manage product recommendations lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="b83cb-105">รายการที่อนุรักษ์คือคอลเลกชันของเนื้อหาแต่ละรายการที่สร้างและอนุรักษ์โดยบุคคล</span><span class="sxs-lookup"><span data-stu-id="b83cb-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="b83cb-106">สร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="b83cb-106">Create a new list</span></span>

<span data-ttu-id="b83cb-107">เมื่อต้องการสร้างรายการแนะนำผลิตภัณฑ์ที่รวบรวมไว้ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b83cb-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="b83cb-108">ไปยัง **Retail และ Commerce &gt; คำแนะนำผลิตภัณฑ์ &gt; รายการคำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="b83cb-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="b83cb-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="b83cb-109">Select **New**.</span></span>
1. <span data-ttu-id="b83cb-110">ในฟิลด์ **รหัสรายการ** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="b83cb-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="b83cb-111">ในฟิลด์ **ชื่อรายการ** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="b83cb-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="b83cb-112">**ชื่อรายการ** คือชื่อเรื่องของรายการที่จะปรากฏในส่วนรายการที่รวบรวมของโมดูล **การรวบรวมผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="b83cb-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="b83cb-113">ในการเพิ่มผลิตภัณฑ์ไปยังรายการ ให้เลือก **เพิ่มผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="b83cb-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="b83cb-114">เมื่อต้องการเปลี่ยนลำดับของผลิตภัณฑ์ในรายการ ให้ป้อนค่าในคอลัมน์ **ใบสั่งที่แสดง**</span><span class="sxs-lookup"><span data-stu-id="b83cb-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="b83cb-115">ถ้าผลิตภัณฑ์สองตัวมีมูลค่าของใบสั่งแสดงผลเดียวกัน ใบสั่งสุดท้ายของผลสองอย่างอาจแตกต่างจากฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="b83cb-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="b83cb-116">เลือก **บันทึก** เพื่อบันทึกรายการ</span><span class="sxs-lookup"><span data-stu-id="b83cb-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="b83cb-117">รายการตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b83cb-117">Example List</span></span>

![รายการการรวบรวมตัวอย่างในฝ่ายสนับสนุน](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="b83cb-119">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b83cb-119">Additional resources</span></span>

[<span data-ttu-id="b83cb-120">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b83cb-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b83cb-121">เปืดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b83cb-121">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="b83cb-122">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b83cb-122">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b83cb-123">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="b83cb-123">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="b83cb-124">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="b83cb-124">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b83cb-125">เพิ่มรายการคำแนะนำลงในไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="b83cb-125">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="b83cb-126">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="b83cb-126">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="b83cb-127">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b83cb-127">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b83cb-128">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="b83cb-128">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="b83cb-129">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="b83cb-129">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="b83cb-130">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b83cb-130">Product recommendations FAQ</span></span>](faq-recommendations.md)
