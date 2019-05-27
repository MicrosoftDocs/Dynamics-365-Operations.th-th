---
title: ประเมินความสามารถในการทำกำไรของลูกค้าและผลิตภัณฑ์
description: บทความนี้อธิบายวิธีที่คุณสามารถใช้การวิเคราะห์แบบในหน่วยความจำหรือแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับข้อมูลเชิงลึกเกี่ยวกับลูกค้าและความสามารถในการทำกำไรของผลิตภัณฑ์จากข้อมูล Microsoft Dynamics 365 for Retail ของคุณ
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
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
ms.openlocfilehash: 28d4eeaa3fcae33f817690ad496b4b123a5838ce
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561375"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="160d8-103">ประเมินความสามารถในการทำกำไรของลูกค้าและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="160d8-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="160d8-104">บทความนี้อธิบายวิธีที่คุณสามารถใช้การวิเคราะห์แบบในหน่วยความจำหรือแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับข้อมูลเชิงลึกเกี่ยวกับลูกค้าและความสามารถในการทำกำไรของผลิตภัณฑ์จากข้อมูล Microsoft Dynamics 365 for Retail ของคุณ</span><span class="sxs-lookup"><span data-stu-id="160d8-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="160d8-105">ในฐานะที่เป็นส่วนหนึ่งของ Dynamics 365 for Retail ผู้ใช้สามารถศึกษาความสามารถในการทำกำไรสำหรับลูกค้าอันดับบน (10 ถึง 100) ในระดับต่างๆ ของลำดับชั้นองค์กร ตามหนึ่งในเกณฑ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="160d8-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="160d8-106">ยอดขาย</span><span class="sxs-lookup"><span data-stu-id="160d8-106">Sales amount</span></span>
- <span data-ttu-id="160d8-107">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="160d8-107">Quantity</span></span>
- <span data-ttu-id="160d8-108">อัตรากำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="160d8-108">Gross profit margin</span></span>
- <span data-ttu-id="160d8-109">เปอร์เซ็นต์กำไร</span><span class="sxs-lookup"><span data-stu-id="160d8-109">Margin percentage</span></span>

<span data-ttu-id="160d8-110">สำหรับการประเมินนี้ คุณสามารถใช้รายงาน **ลูกค้าอันดับแรก** แบบ out-of-box ซึ่งคุณสามารถเปิดได้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="160d8-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="160d8-111">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **Reports** &gt; **รายงานลูกค้าอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="160d8-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="160d8-112">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานลูกค้าอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="160d8-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="160d8-113">ในทำนองเดียวกัน ผู้ใช้สามารถศึกษาผลกำไรสำหรับผลิตภัณฑ์อันดับแรก (10 ถึง 100) ระหว่างระดับต่างๆของลำดับชั้นขององค์กร ที่ขึ้นอยู่กับเงื่อนไขข้อใดข้อหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="160d8-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="160d8-114">ยอดขาย</span><span class="sxs-lookup"><span data-stu-id="160d8-114">Sales amount</span></span>
- <span data-ttu-id="160d8-115">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="160d8-115">Quantity</span></span>
- <span data-ttu-id="160d8-116">อัตรากำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="160d8-116">Gross profit margin</span></span>
- <span data-ttu-id="160d8-117">เปอร์เซ็นต์กำไร</span><span class="sxs-lookup"><span data-stu-id="160d8-117">Margin percentage</span></span>

<span data-ttu-id="160d8-118">สำหรับการประเมินนี้ คุณสามารถใช้รายงาน **ผลิตภัณฑ์อันดับแรก**แบบ out-of-box ซึ่งคุณสามารถเปิดได้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="160d8-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="160d8-119">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **Reports** &gt; **รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="160d8-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="160d8-120">**การจัดการประเภทและผลิตภัณฑ์** พื้นที่ทำงาน &gt; **การขายปลีก** &gt; **ผลิตภัณฑ์และประเภท** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="160d8-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="160d8-121">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="160d8-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
