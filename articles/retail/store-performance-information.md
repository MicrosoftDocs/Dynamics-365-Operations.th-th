---
title: วิเคราะห์ประสิทธิภาพร้านค้า
description: บทความนี้อธิบายวิธีที่คุณสามารถใช้การวิเคราะห์แบบในหน่วยความจำหรือแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับข้อมูลเชิงลึกเกี่ยวกับประสิทธิภาพร้านค้า โดยขึ้นกับ Microsoft Dynamics 365 for Retail ของคุณ
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c975c021b6db49d1e25fd036f4955c7223e438ea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "346191"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="5a242-103">วิเคราะห์ประสิทธิภาพร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5a242-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5a242-104">บทความนี้อธิบายวิธีที่คุณสามารถใช้การวิเคราะห์แบบในหน่วยความจำหรือแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับข้อมูลเชิงลึกเกี่ยวกับประสิทธิภาพร้านค้า โดยขึ้นกับ Microsoft Dynamics 365 for Retail ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5a242-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="5a242-105">ในฐานะที่เป็นส่วนหนึ่งของ Dynamics 365 for Retail ผู้ใช้สามารถศึกษาประสิทธิภาพร้านค้าได้แบบเรียลไทม์ในระดับต่างๆ ของลำดับชั้นองค์กรตลอดช่วงเวลาที่เลือกโดยการเปิดรายงาน **สรุปช่องทาง** แบบสำเร็จรูปจากสถานที่ใดๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5a242-105">As part of Dynamics 365 for Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="5a242-106">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **Reports** &gt; **รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="5a242-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="5a242-107">**การเงินของร้านค้าปลีก** พื้นที่ทำงาน &gt; **Retail** &gt; **ช่องทาง** &gt; **การเงินของร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="5a242-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="5a242-108">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="5a242-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="5a242-109">รายงานนี้แสดงสแนปช็อตของข้อสรุปต่อไปนี้ซึ่งเป็นส่วนหนึ่งของประสิทธิภาพการทำงานของร้านค้า:</span><span class="sxs-lookup"><span data-stu-id="5a242-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="5a242-110">สรุปยอดขายรวม</span><span class="sxs-lookup"><span data-stu-id="5a242-110">Gross sales summary</span></span>
- <span data-ttu-id="5a242-111">สรุปชนิดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="5a242-111">Tender type summary</span></span>
- <span data-ttu-id="5a242-112">สรุปภาษี</span><span class="sxs-lookup"><span data-stu-id="5a242-112">Tax summary</span></span>
- <span data-ttu-id="5a242-113">สรุปการแทนที่ราคา</span><span class="sxs-lookup"><span data-stu-id="5a242-113">Price overrides summary</span></span>
- <span data-ttu-id="5a242-114">สรุปส่วนลด</span><span class="sxs-lookup"><span data-stu-id="5a242-114">Discounts summary</span></span>
