---
title: วิเคราะห์แนวโน้มและรูปแบบการขาย
description: คุณสามารถศึกษาแนวโน้มและรูปแบบการขายได้แบบเรียลไทม์ใน Microsoft Dynamics 365 for Retail
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
ms.openlocfilehash: 7ea5efd1fcde233145e97aea30d312bbe70b20ac
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "358013"
---
# <a name="analyze-sales-trends-and-patterns"></a><span data-ttu-id="03fdf-103">วิเคราะห์แนวโน้มและรูปแบบการขาย</span><span class="sxs-lookup"><span data-stu-id="03fdf-103">Analyze sales trends and patterns</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03fdf-104">คุณสามารถศึกษาแนวโน้มและรูปแบบการขายได้แบบเรียลไทม์ใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="03fdf-104">You can study sales trends and patterns in real time in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="03fdf-105">ในฐานะที่เป็นส่วนหนึ่งของ Dynamics 365 for Retail ผู้ใช้สามารถศึกษาแนวโน้มและรูปแบบการขายได้แบบเรียลไทม์ในระดับต่างๆ ของลำดับชั้นองค์กรตลอดทั้งปีโดยการใช้รายงาน **การขายช่องทางตามปี** แบบสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="03fdf-105">As part of Dynamics 365 for Retail, users can study sales trends and patterns in real time across different levels of the organization hierarchy over a period of years by using the out-of-box **Channel sales by year** report.</span></span> <span data-ttu-id="03fdf-106">คุณสามารถเปิดรายงานนี้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="03fdf-106">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="03fdf-107">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="03fdf-107">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="03fdf-108">**การเงินของร้านค้าปลีก** พื้นที่ทำงาน &gt; **Retail** &gt; **ช่องทาง** &gt; **การเงินของร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="03fdf-108">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="03fdf-109">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="03fdf-109">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by year report**</span></span>

<span data-ttu-id="03fdf-110">ผู้ใช้ยังสามารถศึกษาแนวโน้มและรูปแบบตามชั่วโมงระหว่างลำดับชั้นขององค์กรระดับต่างๆ ณ รอบระยะเวลาที่เลือก โดยใช้รายงาน **รายงานการขายผ่านช่องทางตามชั่วโมง** นอกกรอบ</span><span class="sxs-lookup"><span data-stu-id="03fdf-110">Users can also study sales trends and patterns by hour across different levels of the organization hierarchy over a selected period by using the out-of-box **Channel sales by hour** report.</span></span> <span data-ttu-id="03fdf-111">คุณสามารถเปิดรายงานนี้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="03fdf-111">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="03fdf-112">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="03fdf-112">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="03fdf-113">**การเงินของร้านค้าปลีก** พื้นที่ทำงาน &gt; **Retail** &gt; **ช่องทาง** &gt; **การเงินของร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="03fdf-113">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="03fdf-114">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานการขายผ่านช่องทางตามปีชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="03fdf-114">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by hour report**</span></span>
