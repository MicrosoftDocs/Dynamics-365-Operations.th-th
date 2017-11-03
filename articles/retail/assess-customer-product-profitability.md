---
title: "ประเมินความสามารถในการทำกำไรของลูกค้าและผลิตภัณฑ์"
description: "บทความนี้อธิบายวิธีใช้การวิเคราะห์ในหน่วยความจำแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับความช่วยเหลือเกี่ยวกับลูกค้าและกำไรจากสินค้าจากข้อมูลของ Microsoft Dynamics 365 for Retail"
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 04ebc624212e6909eda7589b71cd84a22010e721
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="da214-103">ประเมินความสามารถในการทำกำไรของลูกค้าและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="da214-103">Assess customer and product profitability</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="da214-104">บทความนี้อธิบายวิธีใช้การวิเคราะห์ในหน่วยความจำแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับความช่วยเหลือเกี่ยวกับลูกค้าและกำไรจากสินค้าจากข้อมูลของ Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="da214-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="da214-105">เนื่องจากเป็นส่วนหนึ่งของ Dynamics 365 for Retail ผู้ใช้สามารถศึกษาผลกำไรสำหรับลูกค้าอันดับแรก (10 ถึง 100) ระหว่างระดับต่างๆของลำดับชั้นขององค์กร ที่ขึ้นอยู่กับเงื่อนไขข้อใดข้อหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="da214-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="da214-106">ยอดขาย</span><span class="sxs-lookup"><span data-stu-id="da214-106">Sales amount</span></span>
-   <span data-ttu-id="da214-107">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="da214-107">Quantity</span></span>
-   <span data-ttu-id="da214-108">อัตรากำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="da214-108">Gross profit margin</span></span>
-   <span data-ttu-id="da214-109">เปอร์เซ็นต์กำไร</span><span class="sxs-lookup"><span data-stu-id="da214-109">Margin percentage</span></span>

<span data-ttu-id="da214-110">สำหรับการประเมินนี้ คุณสามารถใช้รายงาน **ลูกค้าอันดับแรก** แบบ out-of-box ซึ่งคุณสามารถเปิดได้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="da214-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="da214-111">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **Reports** &gt; **รายงานลูกค้าอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="da214-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
-   <span data-ttu-id="da214-112">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานลูกค้าอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="da214-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="da214-113">ในทำนองเดียวกัน ผู้ใช้สามารถศึกษาผลกำไรสำหรับผลิตภัณฑ์อันดับแรก (10 ถึง 100) ระหว่างระดับต่างๆของลำดับชั้นขององค์กร ที่ขึ้นอยู่กับเงื่อนไขข้อใดข้อหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="da214-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="da214-114">ยอดขาย</span><span class="sxs-lookup"><span data-stu-id="da214-114">Sales amount</span></span>
-   <span data-ttu-id="da214-115">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="da214-115">Quantity</span></span>
-   <span data-ttu-id="da214-116">อัตรากำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="da214-116">Gross profit margin</span></span>
-   <span data-ttu-id="da214-117">เปอร์เซ็นต์กำไร</span><span class="sxs-lookup"><span data-stu-id="da214-117">Margin percentage</span></span>

<span data-ttu-id="da214-118">สำหรับการประเมินนี้ คุณสามารถใช้รายงาน **ผลิตภัณฑ์อันดับแรก**แบบ out-of-box ซึ่งคุณสามารถเปิดได้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="da214-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="da214-119">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **Reports** &gt; **รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="da214-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="da214-120">**การจัดการประเภทและผลิตภัณฑ์** พื้นที่ทำงาน &gt; **การขายปลีก** &gt; **ผลิตภัณฑ์และประเภท** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="da214-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="da214-121">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="da214-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>




