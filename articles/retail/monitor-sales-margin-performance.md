---
title: "ตรวจสอบประสิทธิภาพของการขายและกำไรขั้นต้น"
description: "คุณสามารถตรวจสอบประสิทธิภาพการขายและกำไรขั้นต้นในเวลาจริงใน Microsoft Dynamics 365 for Retail"
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 4ba1fb165f873b07f7a6a2286617d873b245ccbf
ms.contentlocale: th-th
ms.lasthandoff: 01/18/2018

---

# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="9bb37-103">ตรวจสอบประสิทธิภาพของการขายและกำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="9bb37-103">Monitor sales and margin performance</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="9bb37-104">คุณสามารถตรวจสอบประสิทธิภาพการขายและกำไรขั้นต้นในเวลาจริงใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="9bb37-104">You can monitor sales and margin performance in real time using Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="9bb37-105">เป็นส่วนหนึ่งของ Dynamics 365 for Retail ผู้ใช้สามารถติดตามการขายและกำไรขั้นต้นในแบบเรียลไทม์ระหว่างระดับต่างๆ ในลำดับชั้นขององค์กรสำหรับมิติต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9bb37-105">As part of Dynamics 365 for Retail, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

-   <span data-ttu-id="9bb37-106">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9bb37-106">Products</span></span>
-   <span data-ttu-id="9bb37-107">ประเภท</span><span class="sxs-lookup"><span data-stu-id="9bb37-107">Categories</span></span>
-   <span data-ttu-id="9bb37-108">ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="9bb37-108">Discounts</span></span>
-   <span data-ttu-id="9bb37-109">ระยะเวลาเป็นปี</span><span class="sxs-lookup"><span data-stu-id="9bb37-109">Years as time period</span></span>
-   <span data-ttu-id="9bb37-110">เครื่องบันทึกเงินสด/เทอร์มินัล</span><span class="sxs-lookup"><span data-stu-id="9bb37-110">Registers/terminals</span></span>
-   <span data-ttu-id="9bb37-111">เจ้าหน้าที่/พนักงาน</span><span class="sxs-lookup"><span data-stu-id="9bb37-111">Staff/employees</span></span>
-   <span data-ttu-id="9bb37-112">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9bb37-112">Customers</span></span>
-   <span data-ttu-id="9bb37-113">หน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="9bb37-113">Operating units</span></span>

<span data-ttu-id="9bb37-114">นอกจากนี้ สองรายงานเฉพาะที่ใช้ประโยชน์จากการจัดโครงสร้างกริดตามลำดับชั้นช่วยให้ผู้ใช้สามารถติดตามประสิทธิภาพการขายและกำไรขั้นต้น โดยการเลื่อนลงจากโหนดประเภทระดับบนสุดเป็นโหนดปลายสุดแต่ละประเภทในลำดับชั้นประเภทผลิตภัณฑ์ขายปลีกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9bb37-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default retail product category hierarchy.</span></span> <span data-ttu-id="9bb37-115">นอกจากนี้ ผู้ใช้อาจเลื่อนจากหน่วยปฏิบัติงานบนสุดไปยังช่องทางแต่ละรายการในลำดับชั้นขององค์กรที่กำหนดไว้เป็นลำดับชั้นขององค์กรเริ่มต้นสำหรับการรายงานวัตถุประสงค์ลำดับชั้นการขายปลีก สำหรับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="9bb37-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for retail reporting hierarchy purposes.</span></span> <span data-ttu-id="9bb37-116">คุณสามารถเปิดรายงานนี้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9bb37-116">You can open the reports from any of the following locations:</span></span>

-   <span data-ttu-id="9bb37-117">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน &gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="9bb37-117">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports**</span></span>
-   <span data-ttu-id="9bb37-118">**การจัดการประเภทและผลิตภัณฑ์** พื้นที่ทำงาน &gt; **การขายปลีก** &gt; **ผลิตภัณฑ์และประเภท** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="9bb37-118">**Category and product management** workspace &gt; **Retail** &gt; **Product and categories** &gt; **Retail store management** &gt; **Reports**</span></span>
-   <span data-ttu-id="9bb37-119">**การจัดการราคาและส่วนลด** พื้นที่ทำงาน &gt; **Retail** &gt; **การจัดการราคาและส่วนลด** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="9bb37-119">**Pricing and discount management** workspace &gt; **Retail** &gt; **Pricing and discounts** &gt; **Retail store management** &gt; **Reports**</span></span>
-   <span data-ttu-id="9bb37-120">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย**</span><span class="sxs-lookup"><span data-stu-id="9bb37-120">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>



