---
title: ประเมินความสามารถในการทำกำไรของลูกค้าและผลิตภัณฑ์
description: บทความนี้อธิบายวิธีที่คุณสามารถใช้การวิเคราะห์แบบในหน่วยความจำหรือแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับข้อมูลเชิงลึกเกี่ยวกับลูกค้าและความสามารถในการทำกำไรของผลิตภัณฑ์จากข้อมูล Dynamics 365 Commerce ของคุณ
author: ashishmsft
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 80a2f38f2b3f039b17556116d6aea738faa1db50
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797340"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="49437-103">ประเมินความสามารถในการทำกำไรของลูกค้าและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="49437-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49437-104">บทความนี้อธิบายวิธีที่คุณสามารถใช้การวิเคราะห์แบบในหน่วยความจำหรือแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับข้อมูลเชิงลึกเกี่ยวกับลูกค้าและความสามารถในการทำกำไรของผลิตภัณฑ์จากข้อมูล Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="49437-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="49437-105">ส่วนหนึ่งของ Commerce ผู้ใช้สามารถศึกษาความสามารถในการทำกำไรสำหรับลูกค้าอันดับบน (10 ถึง 100) ในระดับต่างๆ ของลำดับชั้นองค์กร ตามหนึ่งในเกณฑ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49437-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="49437-106">ยอดขาย</span><span class="sxs-lookup"><span data-stu-id="49437-106">Sales amount</span></span>
- <span data-ttu-id="49437-107">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="49437-107">Quantity</span></span>
- <span data-ttu-id="49437-108">อัตรากำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="49437-108">Gross profit margin</span></span>
- <span data-ttu-id="49437-109">เปอร์เซ็นต์กำไร</span><span class="sxs-lookup"><span data-stu-id="49437-109">Margin percentage</span></span>

<span data-ttu-id="49437-110">สำหรับการประเมินนี้ คุณสามารถใช้รายงาน **ลูกค้าอันดับแรก** แบบ out-of-box ซึ่งคุณสามารถเปิดได้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49437-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="49437-111">**การจัดการร้านค้า** พื้นที่ทำงาน&gt; **Retail และ Commerce** &gt; **ช่องทาง** &gt; **การจัดการร้านค้า** &gt; **Reports** &gt; **รายงานลูกค้าอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="49437-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="49437-112">**การสอบถามและรายงาน** &gt; **การขายปลีกและการค้า** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานลูกค้าอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="49437-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="49437-113">ในทำนองเดียวกัน ผู้ใช้สามารถศึกษาผลกำไรสำหรับผลิตภัณฑ์อันดับแรก (10 ถึง 100) ระหว่างระดับต่างๆของลำดับชั้นขององค์กร ที่ขึ้นอยู่กับเงื่อนไขข้อใดข้อหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49437-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="49437-114">ยอดขาย</span><span class="sxs-lookup"><span data-stu-id="49437-114">Sales amount</span></span>
- <span data-ttu-id="49437-115">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="49437-115">Quantity</span></span>
- <span data-ttu-id="49437-116">อัตรากำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="49437-116">Gross profit margin</span></span>
- <span data-ttu-id="49437-117">เปอร์เซ็นต์กำไร</span><span class="sxs-lookup"><span data-stu-id="49437-117">Margin percentage</span></span>

<span data-ttu-id="49437-118">สำหรับการประเมินนี้ คุณสามารถใช้รายงาน **ผลิตภัณฑ์อันดับแรก** แบบ out-of-box ซึ่งคุณสามารถเปิดได้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49437-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="49437-119">**การจัดการร้านค้า** พื้นที่ทำงาน&gt; **Retail และ Commerce** &gt; **ช่องทาง** &gt; **การจัดการร้านค้า** &gt; **Reports** &gt; **รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="49437-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="49437-120">**การจัดการประเภทและผลิตภัณฑ์** พื้นที่ทำงาน &gt; **การขายปลีกและการค้า** &gt; **ผลิตภัณฑ์และประเภท** &gt; **การจัดการร้านค้า** &gt; **รายงาน** &gt; **รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="49437-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="49437-121">**การสอบถามและรายงาน** &gt; **การขายปลีกและการค้า** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="49437-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]