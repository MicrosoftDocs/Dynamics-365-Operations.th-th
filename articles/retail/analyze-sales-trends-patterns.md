---
title: "วิเคราะห์แนวโน้มและรูปแบบการขาย"
description: "คุณสามารถศึกษาแนวโน้มการและรูปแบบในเวลาจริงใน Microsoft Dynamics 365 for Retail"
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailChannelReport, SysReportViewerForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 84d0eda16b4f3d8570d3594a06e6ddb7eb4717c9
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---

# <a name="analyze-sales-trends-and-patterns"></a><span data-ttu-id="4b53d-103">วิเคราะห์แนวโน้มและรูปแบบการขาย</span><span class="sxs-lookup"><span data-stu-id="4b53d-103">Analyze sales trends and patterns</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4b53d-104">คุณสามารถศึกษาแนวโน้มการและรูปแบบในเวลาจริงใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="4b53d-104">You can study sales trends and patterns in real time in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="4b53d-105">เนื่องจากเป็นส่วนหนึ่งของ Dynamics 365 for Retail ผู้ใช้สามารถศึกษาแนวโน้มและรูปแบบการขายในเวลาจริงระหว่างลำดับชั้นขององค์กรระดับต่างๆ ณ รอบระยะเวลาของปี โดยใช้รายงาน **การขายผ่านช่องทางตามปี** นอกกรอบ</span><span class="sxs-lookup"><span data-stu-id="4b53d-105">As part of Dynamics 365 for Retail, users can study sales trends and patterns in real time across different levels of the organization hierarchy over a period of years by using the out-of-box **Channel sales by year** report.</span></span> <span data-ttu-id="4b53d-106">คุณสามารถเปิดรายงานนี้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4b53d-106">You can open this report from any of the following locations:</span></span>

-   <span data-ttu-id="4b53d-107">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="4b53d-107">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
-   <span data-ttu-id="4b53d-108">**การเงินของร้านค้าปลีก** พื้นที่ทำงาน &gt; **Retail** &gt; **ช่องทาง** &gt; **การเงินของร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="4b53d-108">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
-   <span data-ttu-id="4b53d-109">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="4b53d-109">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by year report**</span></span>

<span data-ttu-id="4b53d-110">ผู้ใช้ยังสามารถศึกษาแนวโน้มและรูปแบบตามชั่วโมงระหว่างลำดับชั้นขององค์กรระดับต่างๆ ณ รอบระยะเวลาที่เลือก โดยใช้รายงาน **รายงานการขายผ่านช่องทางตามชั่วโมง** นอกกรอบ</span><span class="sxs-lookup"><span data-stu-id="4b53d-110">Users can also study sales trends and patterns by hour across different levels of the organization hierarchy over a selected period by using the out-of-box **Channel sales by hour** report.</span></span> <span data-ttu-id="4b53d-111">คุณสามารถเปิดรายงานนี้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4b53d-111">You can open this report from any of the following locations:</span></span>

-   <span data-ttu-id="4b53d-112">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="4b53d-112">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
-   <span data-ttu-id="4b53d-113">**การเงินของร้านค้าปลีก** พื้นที่ทำงาน &gt; **Retail** &gt; **ช่องทาง** &gt; **การเงินของร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="4b53d-113">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
-   <span data-ttu-id="4b53d-114">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานการขายผ่านช่องทางตามปีชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="4b53d-114">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by hour report**</span></span>



