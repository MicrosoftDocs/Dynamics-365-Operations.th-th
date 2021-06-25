---
title: เปิดใช้งานข้อเสนองบประมาณ (ตัวอย่าง)
description: หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานข้อเสนองบประมาณในข้อมูลเชิงลึกทางการเงิน
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222545"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="f5ba6-103">เปิดใช้งานข้อเสนองบประมาณ (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="f5ba6-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f5ba6-104">หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานข้อเสนองบประมาณในข้อมูลเชิงลึกทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="f5ba6-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="f5ba6-105">ใช้ข้อมูลจากหน้าสภาพแวดล้อมใน Microsoft Dynamics Lifecycle Services (LCS) เพื่อเชื่อมต่อกับอินสแตนซ์หลักของ AZURE SQL สำหรับสภาพแวดล้อมดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="f5ba6-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="f5ba6-106">รันคำสั่ง Transact-SQL (T-SQL) ต่อไปนี้เพื่อเปิดใช้งานเที่ยวบินสำหรับสภาพแวดล้อม sandbox</span><span class="sxs-lookup"><span data-stu-id="f5ba6-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="f5ba6-107">(คุณอาจต้องเปิดใช้งานการเข้าถึงสำหรับที่อยู่ IP ของคุณใน LCS ก่อนที่คุณจะสามารถเชื่อมต่อระยะไกลกับเซิร์ฟเวอออบเจ็กต์โปรแกรมประยุกต์ \[AOS\])</span><span class="sxs-lookup"><span data-stu-id="f5ba6-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="f5ba6-108">ข้ามขั้นตอนนี้ถ้าคุณใช้รุ่น 10.0.20 หรือใหม่กว่า หรือถ้าคุณใช้งานการปรับใช้ Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f5ba6-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="f5ba6-109">ทีมงานในเชิงลึกของการเงินควรมีการเปิดใช้งานเที่ยวบินให้คุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="f5ba6-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="f5ba6-110">ถ้าคุณไม่เห็นคุณลักษณะในพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** หรือหากประสบปัญหาเมื่อคุณพยายามเปิดใช้งาน โปรดติดต่อ <fiap@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="f5ba6-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="f5ba6-111">เปิดพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** และปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f5ba6-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="f5ba6-112">เลือก **ตรวจหาการอัพเดต**</span><span class="sxs-lookup"><span data-stu-id="f5ba6-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="f5ba6-113">ค้นหา **ข้อเสนองบประมาณ** และเปิดใช้งานลักษณะการทำงานนั้น</span><span class="sxs-lookup"><span data-stu-id="f5ba6-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="f5ba6-114">ไปที่ **การจัดงบประมาณ \> การตั้งค่า \> การจัดงบประมาณพื้นฐาน \> ข้อเสนองบประมาณ (ตัวอย่าง)** และเลือก **เปิดใช้งานคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="f5ba6-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
