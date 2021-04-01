---
title: วิเคราะห์ประสิทธิภาพร้านค้า
description: บทความนี้อธิบายวิธีที่คุณสามารถใช้การวิเคราะห์แบบในหน่วยความจำหรือแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับข้อมูลเชิงลึกเกี่ยวกับประสิทธิภาพร้านค้า โดยขึ้นกับ Dynamics 365 Commerce ของคุณ
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
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: aced862e279135e25ca7380b746ae19b97227d10
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234256"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="b269a-103">วิเคราะห์ประสิทธิภาพร้านค้า</span><span class="sxs-lookup"><span data-stu-id="b269a-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b269a-104">บทความนี้อธิบายวิธีที่คุณสามารถใช้การวิเคราะห์แบบในหน่วยความจำหรือแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับข้อมูลเชิงลึกเกี่ยวกับประสิทธิภาพร้านค้า โดยขึ้นกับ Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b269a-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="b269a-105">ส่วนหนึ่งของ Retail ผู้ใช้สามารถศึกษาประสิทธิภาพร้านค้าได้แบบเรียลไทม์ในระดับต่างๆ ของลำดับชั้นองค์กรตลอดช่วงเวลาที่เลือกโดยการเปิดรายงาน **สรุปช่องทาง** แบบสำเร็จรูปจากสถานที่ใดๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b269a-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="b269a-106">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **Reports** &gt; **รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="b269a-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="b269a-107">**การเงินของร้านค้าปลีก** พื้นที่ทำงาน &gt; **Retail** &gt; **ช่องทาง** &gt; **การเงินของร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="b269a-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="b269a-108">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="b269a-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="b269a-109">รายงานนี้แสดงสแนปช็อตของข้อสรุปต่อไปนี้ซึ่งเป็นส่วนหนึ่งของประสิทธิภาพการทำงานของร้านค้า:</span><span class="sxs-lookup"><span data-stu-id="b269a-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="b269a-110">สรุปยอดขายรวม</span><span class="sxs-lookup"><span data-stu-id="b269a-110">Gross sales summary</span></span>
- <span data-ttu-id="b269a-111">สรุปชนิดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b269a-111">Tender type summary</span></span>
- <span data-ttu-id="b269a-112">สรุปภาษี</span><span class="sxs-lookup"><span data-stu-id="b269a-112">Tax summary</span></span>
- <span data-ttu-id="b269a-113">สรุปการแทนที่ราคา</span><span class="sxs-lookup"><span data-stu-id="b269a-113">Price overrides summary</span></span>
- <span data-ttu-id="b269a-114">สรุปส่วนลด</span><span class="sxs-lookup"><span data-stu-id="b269a-114">Discounts summary</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]