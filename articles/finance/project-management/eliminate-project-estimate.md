---
title: ตัดการประเมินโครงการออก
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับการตัดการประเมินโครงการออก หลังจากเสร็จสมบูรณ์แล้ว
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410270"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="08d88-103">ตัดการประเมินโครงการออก</span><span class="sxs-lookup"><span data-stu-id="08d88-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08d88-104">การประเมินโครงการแสดงมุมมองทางการเงินสำหรับงานที่ถูกประเมินและถูกจัดกำหนดการไว้สำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="08d88-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="08d88-105">ถ้าคุณต้องการทำงานกับการประเมินสำหรับโครงการ คุณต้องแนบโครงการกับโครงการประเมิน</span><span class="sxs-lookup"><span data-stu-id="08d88-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="08d88-106">โครงการประเมินจะขึ้นอยู่กับโครงการที่มีอยู่เสมอ อย่างไรก็ตาม โครงการหลายโครงการสามารถอ้างอิงถึงโครงการประเมินเดียว</span><span class="sxs-lookup"><span data-stu-id="08d88-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="08d88-107">เฉพาะโครงการที่มีราคาคงที่และโครงการลงทุนเท่านั้นที่สามารถแนบกับโครงการประเมินได้ และโครงการเหล่านั้นจะต้องอยู่ในกลุ่มโครงการเดียวกันกับโครงการประเมิน</span><span class="sxs-lookup"><span data-stu-id="08d88-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="08d88-108">เมื่อต้องการกำจัดโครงการประเมิน ต้องทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="08d88-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="08d88-109">ขั้นตอนต่อไปนี้อธิบายวิธีการตัดการประเมินออก</span><span class="sxs-lookup"><span data-stu-id="08d88-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="08d88-110">ไปที่ **การจัดการและการบัญชีโครงการ** > **โครงการทั้งหมด** และเปิดโครงการ</span><span class="sxs-lookup"><span data-stu-id="08d88-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="08d88-111">บนแท็บ **จัดการ** เลือก **การประเมิน** และบนหน้า **การประเมิน** เลือก **ตัดออก**</span><span class="sxs-lookup"><span data-stu-id="08d88-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="08d88-112">บนหน้า **ตัดการประเมินออก** บนแท็บ **ทั่วไป** ให้ตั้งค่าตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="08d88-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="08d88-113">**รหัสรอบระยะเวลา**: เลือกรหัสรอบระยะเวลาเพื่อเลือกโครงการประเมินที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="08d88-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="08d88-114">**วันที่ประเมิน**: เลือกวันที่ประเมินที่เหมาะสมสำหรับการตัดออก</span><span class="sxs-lookup"><span data-stu-id="08d88-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="08d88-115">**ตัดออกพร้อมคำเตือน WIP**: เปิดใช้งานตัวเลือกนี้เพื่อให้การแจ้งเตือนเวลาที่การประเมินที่เกี่ยวข้องกับงานระหว่างทำ (WIP) จะถูกตัดออก</span><span class="sxs-lookup"><span data-stu-id="08d88-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="08d88-116">เมื่อไม่มีการเปิดใช้งานตัวเลือกนี้ การตัดออกจะไม่สามารถดำเนินการต่อได้ ถ้ามีธุรกรรมที่ไม่ได้ประเมินใดๆ อยู่</span><span class="sxs-lookup"><span data-stu-id="08d88-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="08d88-117">ตัวเลือกนี้จะพร้อมใช้งานเฉพาะเมื่อมีการใช้การตัดออกกับโครงการประเมินเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="08d88-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="08d88-118">ฟิลด์นี้จะไม่พร้อมใช้งาน ถ้าคุณกำลังใช้การลงรายการบัญชีประจำงวด</span><span class="sxs-lookup"><span data-stu-id="08d88-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="08d88-119">การตั้งค่านี้จะทำงานกับการตั้งค่าบนแท็บ **การประเมิน** บนหน้า **พารามิเตอร์โครงการ** ในกลุ่มฟิลด์ **อนุญาตให้ตัดออกได้ เมื่อมีธุรกรรมที่ไม่ได้ประเมินอยู่**</span><span class="sxs-lookup"><span data-stu-id="08d88-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="08d88-120">**ตั้งค่าขั้นเป็นเสร็จสิ้น**: เปิดใช้งานตัวเลือกนี้เพื่อตั้งค่าขั้นของโครงการประเมินเป็น **เสร็จสมบูรณ์** หลังจากที่คุณรันการตัดออก</span><span class="sxs-lookup"><span data-stu-id="08d88-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="08d88-121">**พิมพ์รายการประเมิน**: เลือกข้อมูลที่จะรวม เมื่อมีการพิมพ์รายการประเมิน</span><span class="sxs-lookup"><span data-stu-id="08d88-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="08d88-122">**แสดง Infolog**: เปิดใช้งานตัวเลือกนี้เพื่อแสดง Infolog</span><span class="sxs-lookup"><span data-stu-id="08d88-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="08d88-123">**วันที่ลงรายการบัญชี**: เลือกวันที่ลงรายการบัญชีแยกประเภทของการประเมิน</span><span class="sxs-lookup"><span data-stu-id="08d88-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="08d88-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="08d88-124">Select **OK**.</span></span>
5. <span data-ttu-id="08d88-125">หลังจากเสร็จสิ้นกระบวนการตัดออก จะมีการแสดงโครงการประเมินที่ตัดออกด้วยค่าลบ</span><span class="sxs-lookup"><span data-stu-id="08d88-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="08d88-126">ถ้าคุณไม่ได้ตั้งใจที่จะตัดการประเมิน คุณสามารถเลือกการประเมินที่ตัดออกและเลือก **กลับรายการการตัดออก**</span><span class="sxs-lookup"><span data-stu-id="08d88-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
