---
title: "วิเคราะห์ประสิทธิภาพร้านค้า"
description: "บทความนี้อธิบายวิธีใช้การวิเคราะห์ในหน่วยความจำแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับความช่วยเหลือเกี่ยวกับประสิทธิภาพร้านค้าจากข้อมูลของ Microsoft Dynamics 365 for Retail"
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5cb5881cdb9c769bfc4272da85bc1c886a36705b
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="analyze-store-performance"></a><span data-ttu-id="df617-103">วิเคราะห์ประสิทธิภาพร้านค้า</span><span class="sxs-lookup"><span data-stu-id="df617-103">Analyze store performance</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="df617-104">บทความนี้อธิบายวิธีใช้การวิเคราะห์ในหน่วยความจำแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับความช่วยเหลือเกี่ยวกับประสิทธิภาพร้านค้าจากข้อมูลของ Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="df617-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="df617-105">เนื่องจากเป็นส่วนหนึ่งของ Dynamics 365 for Retail ผู้ใช้สามารถศึกษาประสิทธิภาพการจัดเก็บในเวลาจริงระหว่างลำดับชั้นขององค์กรระดับต่างๆ ณ รอบระยะเวลาที่เลือก โดยการเปิดรายงาน **สรุปช่องทาง** แบบ out-of-box จากที่ตั้งใดๆต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="df617-105">As part of Dynamics 365 for Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

-   <span data-ttu-id="df617-106">**การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **Reports** &gt; **รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="df617-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
-   <span data-ttu-id="df617-107">**การเงินของร้านค้าปลีก** พื้นที่ทำงาน &gt; **Retail** &gt; **ช่องทาง** &gt; **การเงินของร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="df617-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
-   <span data-ttu-id="df617-108">**การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="df617-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="df617-109">รายงานนี้แสดงสแนปช็อตของข้อสรุปต่อไปนี้ซึ่งเป็นส่วนหนึ่งของประสิทธิภาพการทำงานของร้านค้า:</span><span class="sxs-lookup"><span data-stu-id="df617-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

-   <span data-ttu-id="df617-110">สรุปยอดขายรวม</span><span class="sxs-lookup"><span data-stu-id="df617-110">Gross sales summary</span></span>
-   <span data-ttu-id="df617-111">สรุปชนิดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="df617-111">Tender type summary</span></span>
-   <span data-ttu-id="df617-112">สรุปภาษี</span><span class="sxs-lookup"><span data-stu-id="df617-112">Tax summary</span></span>
-   <span data-ttu-id="df617-113">สรุปการแทนที่ราคา</span><span class="sxs-lookup"><span data-stu-id="df617-113">Price overrides summary</span></span>
-   <span data-ttu-id="df617-114">สรุปส่วนลด</span><span class="sxs-lookup"><span data-stu-id="df617-114">Discounts summary</span></span>



