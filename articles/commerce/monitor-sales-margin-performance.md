---
title: ตรวจสอบประสิทธิภาพของการขายและกำไรขั้นต้น
description: คุณสามารถตรวจสอบประสิทธิภาพการขายและกำไรได้แบบเรียลไทม์โดยใช้ Dynamics 365 Commerce
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 51dc7c4b62a497e3dc9279b3c5a616057316c106
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985897"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="7f324-103">ตรวจสอบประสิทธิภาพของการขายและกำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="7f324-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7f324-104">คุณสามารถตรวจสอบประสิทธิภาพการขายและกำไรได้แบบเรียลไทม์โดยใช้ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7f324-104">You can monitor sales and margin performance in real time using Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7f324-105">ในฐานะที่เป็นส่วนหนึ่งของการค้า ผู้ใช้สามารถตรวจสอบประสิทธิภาพการขายและกำไรขั้นต้นได้แบบเรียลไทม์ในระดับต่างๆของลำดับชั้นขององค์กร สำหรับมิติดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f324-105">As part of Commerce, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="7f324-106">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7f324-106">Products</span></span>
- <span data-ttu-id="7f324-107">ประเภท</span><span class="sxs-lookup"><span data-stu-id="7f324-107">Categories</span></span>
- <span data-ttu-id="7f324-108">ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="7f324-108">Discounts</span></span>
- <span data-ttu-id="7f324-109">ระยะเวลาเป็นปี</span><span class="sxs-lookup"><span data-stu-id="7f324-109">Years as time period</span></span>
- <span data-ttu-id="7f324-110">เครื่องบันทึกเงินสด/เทอร์มินัล</span><span class="sxs-lookup"><span data-stu-id="7f324-110">Registers/terminals</span></span>
- <span data-ttu-id="7f324-111">เจ้าหน้าที่/พนักงาน</span><span class="sxs-lookup"><span data-stu-id="7f324-111">Staff/employees</span></span>
- <span data-ttu-id="7f324-112">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7f324-112">Customers</span></span>
- <span data-ttu-id="7f324-113">หน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="7f324-113">Operating units</span></span>

<span data-ttu-id="7f324-114">นอกจากนี้ รายงานเฉพาะทั้งสองที่ใช้ประโยชน์จากการจัดโครงสร้างกริดตามลำดับชั้นช่วยให้ผู้ใช้สามารถติดตามประสิทธิภาพการขายและกำไรขั้นต้น โดยการเลื่อนลงจากโหนดประเภทระดับบนสุดเป็นโหนดปลายสุดแต่ละประเภทในการจัดประเภทตามลำดับชั้นผลิตภัณฑ์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7f324-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default product category hierarchy.</span></span> <span data-ttu-id="7f324-115">นอกจากนี้ผู้ใช้อาจเลื่อนจากหน่วยปฏิบัติงานบนสุดไปยังช่องทางแต่ละรายการในลำดับชั้นขององค์กรที่กำหนดไว้เป็นลำดับชั้นขององค์กรเริ่มต้นสำหรับการรายงาน</span><span class="sxs-lookup"><span data-stu-id="7f324-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for reporting.</span></span> <span data-ttu-id="7f324-116">คุณสามารถเปิดรายงานนี้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7f324-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="7f324-117">**การจัดการร้านค้า** พื้นที่ทำงาน &gt; **Retail และ Commerce** &gt; **ช่องทาง** &gt; **การจัดการร้านค้า** &gt; **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="7f324-117">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="7f324-118">**การจัดการประเภทและผลิตภัณฑ์** พื้นที่ทำงาน &gt; **Retail และ Commerce** &gt; **ผลิตภัณฑ์และประเภท** &gt; **การจัดการร้านค้า** &gt; **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="7f324-118">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Product and categories** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="7f324-119">**การจัดการการกำหนดราคาและส่วนลด** พื้นที่ทำงาน &gt; **Retail และ Commerce** &gt; **การกำหนดราคาและส่วนลด** &gt; **การจัดการร้านค้า** &gt; **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="7f324-119">**Pricing and discount management** workspace &gt; **Retail and Commerce** &gt; **Pricing and discounts** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="7f324-120">**การสอบถามและรายงาน** ส่วน &gt; **Retail และ Commerce** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย**</span><span class="sxs-lookup"><span data-stu-id="7f324-120">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>
