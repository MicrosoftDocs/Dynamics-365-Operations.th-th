---
title: วิเคราะห์แนวโน้มและรูปแบบการขาย
description: คุณสามารถศึกษาแนวโน้มและรูปแบบการขายได้แบบเรียลไทม์ใน Dynamics 365 Commerce
author: ashishmsft
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelReport, SysReportViewerForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: bcb805e3c2022a9ee13049456522712e42ef3b51
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797368"
---
# <a name="analyze-sales-trends-and-patterns"></a><span data-ttu-id="5d055-103">วิเคราะห์แนวโน้มและรูปแบบการขาย</span><span class="sxs-lookup"><span data-stu-id="5d055-103">Analyze sales trends and patterns</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5d055-104">คุณสามารถศึกษาแนวโน้มและรูปแบบการขายได้แบบเรียลไทม์ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5d055-104">You can study sales trends and patterns in real time in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5d055-105">ส่วนหนึ่งของ Commerce ผู้ใช้สามารถศึกษาแนวโน้มและรูปแบบการขายได้แบบเรียลไทม์ในระดับต่างๆ ของลำดับชั้นองค์กรได้ตลอดทั้งปีโดยการใช้รายงาน **การขายผ่านช่องทางเรียงตามปี** แบบสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="5d055-105">As part of Commerce, users can study sales trends and patterns in real time across different levels of the organization hierarchy over a period of years by using the out-of-box **Channel sales by year** report.</span></span> <span data-ttu-id="5d055-106">คุณสามารถเปิดรายงานนี้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5d055-106">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="5d055-107">**การจัดการร้านค้า** พื้นที่ทำงาน&gt; **Retail และ Commerce** &gt; **ช่องทาง** &gt; **การจัดการร้านค้า** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="5d055-107">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="5d055-108">**การเงินของร้านค้า** พื้นที่ทำงาน&gt; **Retail และ Commerce** &gt; **ช่องทาง** &gt; **การเงินของร้านค้า** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="5d055-108">**Store financials** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store financials** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="5d055-109">**การสอบถามและรายงาน** ส่วน &gt; **Retail และ Commerce** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานการขายผ่านช่องทางตามปี**</span><span class="sxs-lookup"><span data-stu-id="5d055-109">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by year report**</span></span>

<span data-ttu-id="5d055-110">ผู้ใช้ยังสามารถศึกษาแนวโน้มและรูปแบบตามชั่วโมงระหว่างลำดับชั้นขององค์กรระดับต่างๆ ณ รอบระยะเวลาที่เลือก โดยใช้รายงาน **รายงานการขายผ่านช่องทางตามชั่วโมง** นอกกรอบ</span><span class="sxs-lookup"><span data-stu-id="5d055-110">Users can also study sales trends and patterns by hour across different levels of the organization hierarchy over a selected period by using the out-of-box **Channel sales by hour** report.</span></span> <span data-ttu-id="5d055-111">คุณสามารถเปิดรายงานนี้จากตำแหน่งที่ตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5d055-111">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="5d055-112">**การจัดการร้านค้า** พื้นที่ทำงาน&gt; **Retail และ Commerce** &gt; **ช่องทาง** &gt; **การจัดการร้านค้า** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="5d055-112">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="5d055-113">**การเงินของร้านค้า** พื้นที่ทำงาน&gt; **Retail และ Commerce** &gt; **ช่องทาง** &gt; **การเงินของร้านค้า** &gt; **รายงาน** &gt; **รายงานการขายผ่านช่องทางตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="5d055-113">**Store financials** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store financials** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="5d055-114">**การสอบถามและรายงาน** ส่วน &gt; **Retail และ Commerce** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานการขายผ่านช่องทางตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="5d055-114">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by hour report**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]