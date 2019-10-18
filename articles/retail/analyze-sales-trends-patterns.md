---
title: วิเคราะห์แนวโน้มและรูปแบบการขาย
description: คุณสามารถศึกษาแนวโน้มและรูปแบบการขายได้แบบเรียลไทม์ใน Dynamics 365 Retail
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: c54e707d312d7ac3bbcad71a914e528859038a13
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025828"
---
# <a name="analyze-sales-trends-and-patterns"></a><span data-ttu-id="d8e4b-103">วิเคราะห์แนวโน้มและรูปแบบการขาย</span><span class="sxs-lookup"><span data-stu-id="d8e4b-103">Analyze sales trends and patterns</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d8e4b-104">คุณสามารถศึกษาแนวโน้มและรูปแบบการขายได้แบบเรียลไทม์ใน Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="d8e4b-104">You can study sales trends and patterns in real time in Dynamics 365 Retail.</span></span>

<span data-ttu-id="d8e4b-105">ส่วนหนึ่งของ Retail ผู้ใช้สามารถศึกษาแนวโน้มและรูปแบบการขายได้แบบเรียลไทม์ในระดับต่างๆ ของลำดับชั้นองค์กรได้ตลอดทั้งปีโดยการใช้รายงาน **การขายผ่านช่องทางเรียงตามปี** แบบสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="d8e4b-105">As part of Retail, users can study sales trends and patterns in real time across different levels of the organization hierarchy over a period of years by using the out-of-box **Channel sales by year** report.</span></span> <span data-ttu-id="d8e4b-106">คุณสามารถเปิดรายงานนี้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d8e4b-106">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="d8e4b-107">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="d8e4b-107">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="d8e4b-108">**การเงินของร้านค้าปลีก** พื้นที่ทำงาน &gt; **Retail** &gt; **ช่องทาง** &gt; **การเงินของร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="d8e4b-108">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="d8e4b-109">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="d8e4b-109">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by year report**</span></span>

<span data-ttu-id="d8e4b-110">ผู้ใช้ยังสามารถศึกษาแนวโน้มและรูปแบบตามชั่วโมงระหว่างลำดับชั้นขององค์กรระดับต่างๆ ณ รอบระยะเวลาที่เลือก โดยใช้รายงาน **รายงานการขายผ่านช่องทางตามชั่วโมง** นอกกรอบ</span><span class="sxs-lookup"><span data-stu-id="d8e4b-110">Users can also study sales trends and patterns by hour across different levels of the organization hierarchy over a selected period by using the out-of-box **Channel sales by hour** report.</span></span> <span data-ttu-id="d8e4b-111">คุณสามารถเปิดรายงานนี้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d8e4b-111">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="d8e4b-112">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="d8e4b-112">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="d8e4b-113">**การเงินของร้านค้าปลีก** พื้นที่ทำงาน &gt; **Retail** &gt; **ช่องทาง** &gt; **การเงินของร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="d8e4b-113">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="d8e4b-114">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานการขายผ่านช่องทางตามปีชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="d8e4b-114">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by hour report**</span></span>
