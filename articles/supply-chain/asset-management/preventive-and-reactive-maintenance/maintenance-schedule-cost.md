---
title: ต้นทุนกำหนดการบำรุงรักษา
description: หัวข้อนี้อธิบายถึงต้นทุนกำหนดการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b2f53a4a64b06efc9269c607bfe1fc3a41c90cdd
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922079"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="39047-103">ต้นทุนกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="39047-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="39047-104">ในการจัดการสินทรัพย์ คุณสามารถคำนวณงบประมาณต้นทุนในรายการกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="39047-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="39047-105">การทำเช่นนี้มีประโยชน์ถ้าคุณต้องการดูภาพรวมของต้นทุนที่คาดไว้ ตัวอย่างเช่นต้นทุนที่เกี่ยวข้องกับงานบำรุงรักษาเชิงป้องกันที่วางแผนไว้สำหรับปีถัดไป</span><span class="sxs-lookup"><span data-stu-id="39047-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="39047-106">การคำนวณจะขึ้นอยู่กับรายการกำหนดการบำรุงรักษาที่มีอยู่ของชนิด "แผนการบำรุงรักษา" และ "รอบการบำรุงรักษา" และ "การร้องขอการบำรุงรักษา"</span><span class="sxs-lookup"><span data-stu-id="39047-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="39047-107">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **สินทรัพย์** > **ต้นทุนกำหนดการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="39047-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="39047-108">ในกล่องโต้ตอบ **ต้นทุนกำหนดการบำรุงรักษา** คุณสามารถเลือก **เซ็ตมิติทางการเงิน** ถ้าคุณต้องการดูต้นทุนที่จัดกลุ่มในมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="39047-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="39047-109">เซ็ตมิติทางการเงินจะได้รับการตั้งค่าใน **บัญชีแยกประเภททั่วไป** > **ผังบัญชี** > **มิติ** > **เซ็ตมิติทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="39047-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="39047-110">คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้รายการกำหนดการบำรุงรักษาเกี่ยวกับตำเเหน่งที่ทำงานมากเพียงใด</span><span class="sxs-lookup"><span data-stu-id="39047-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="39047-111">ตัวอย่างเช่น หากคุณใส่หมายเลข "1" ในฟิลด์ และคุณมีโครงสร้างตำเเหน่งที่ทำงานหลายระดับ รายการกำหนดการบำรุงรักษาทั้งหมดสำหรับตำเเหน่งที่ทำงานจะถูกเเสดงบนระดับบนสุดดังนั้นชั่วโมงในรายการอาจจะมีการเพิ่มจากตำเเหน่งที่ทำงานที่อยู่ในระดับที่ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="39047-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="39047-112">หากคุณแทรกหมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงรายการกำหนดการบำรุงรักษาทั้งหมด บนระดับตำเเหน่งที่ทำงานทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="39047-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="39047-113">ถ้าคุณต้องการทำการคำนวณสำหรับสินทรัพย์เฉพาะ คลิก **ตัวกรอง** บนเเท็บด่วน **เรกคอร์ดเพื่อรวม** เเละเลือกสินทรัพย์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="39047-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="39047-114">ถ้าจำเป็น คุณสามารถระบุวันที่ **เริ่มต้นที่คาดไว้** สำหรับการคำนวณต้นทุนหรือเลือก **สถานะ** เเบบอื่นสำหรับการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="39047-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="39047-115">คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="39047-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="39047-116">บนเเท็บ **ต้นทุนกำหนดการบำรุงรักษา** > ในกลุ่มบานหน้าต่างการดำเนินการ **กลุ่มโดย...** คลิกปุ่มที่เกี่ยวข้องเพื่อแสดงระดับรายละเอียดที่จำเป็นของการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="39047-116">On the **Maintenance schedule cost** tab > in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="39047-117">ปุ่มบานหน้าต่างการดำเนินการที่เลือกจะถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="39047-117">The selected action pane group buttons are highlighted.</span></span> <span data-ttu-id="39047-118">คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="39047-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="39047-119">คลิกปุ่ม **การคำนวณต้นทุน** ถ้าคุณต้องการทำการคำนวณต้นทุนใหม่</span><span class="sxs-lookup"><span data-stu-id="39047-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="39047-120">ภาพด้านล่างแสดงผลลัพธ์ของการคำนวณต้นทุนของกำหนดการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="39047-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![รูปที่ 1](media/17-preventive-maintenance.png)

