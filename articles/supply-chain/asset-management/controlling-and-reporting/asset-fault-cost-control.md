---
title: การควบคุมต้นทุนข้อบกพร่องของสินทรัพย์
description: หัวข้อนี้อธิบายถึงการควบคุมต้นทุนข้อบกพร่องของสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c25b3efbd0f2f0ec22a08aeac54ffb7fd9398c83
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253841"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="f4495-103">การควบคุมต้นทุนข้อบกพร่องของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f4495-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f4495-104">ในการจัดการสินทรัพย์ คุณสามารถคำนวณต้นทุนของการลงทะเบียนข้อบกพร่องของสินทรัพย์ เพื่อดูภาพรวมของต้นทุนจริงเปรียบเทียบกับต้นทุนตามงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f4495-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="f4495-105">ต้นทุนจริงจะขึ้นอยู่กับธุรกรรมที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="f4495-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="f4495-106">วันที่ คือวันที่ข้อบกพร่องได้มีการเรกคอร์ดอาการ</span><span class="sxs-lookup"><span data-stu-id="f4495-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="f4495-107">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **ข้อบกพร่องของสินทรัพย์** > **การควบคุมต้นทุนข้อบกพร่องของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="f4495-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="f4495-108">ในกล่องโตัตอบ **การควบคุมต้นทุนข้อบกพร่องของสินทรัพย์** ให้เลือกเซ็ตมิติทางการเงินที่จะรวมไว้ในการคำนวณ หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="f4495-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="f4495-109">เลือก "ใช่" บนปุ่มสลับ **ข้ามเลขศูนย์** ถ้าคุณไม่ต้องการแสดงผลลัพธ์ที่มีต้นทุนเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="f4495-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="f4495-110">คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้รายการการควบคุมต้นทุนเกี่ยวกับตำเเหน่งที่ทำงานมากเพียงใด</span><span class="sxs-lookup"><span data-stu-id="f4495-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="f4495-111">ตัวอย่างเช่น หากคุณใส่หมายเลข "1" ในฟิลด์ และคุณมีโครงสร้างตำเเหน่งที่ทำงานหลายระดับ รายการการควบคุมต้นทุนข้อบกพร่องทั้งหมดสำหรับตำเเหน่งที่ทำงาน จะถูกเเสดงบนระดับบนสุด ดังนั้นชั่วโมงในรายการอาจจะมีการเพิ่มจากตำเเหน่งที่ทำงานที่อยู่ในระดับที่ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="f4495-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="f4495-112">หากคุณใส่หมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงรายการควบคุมต้นทุนข้อบกพร่องทั้งหมด บนระดับตำเเหน่งที่ทำงานทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f4495-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="f4495-113">หากคุณต้องการจำกัดการค้นหา คุณสามารถเลือกสินทรัพย์เฉพาะ วันที่บกพร่อง สาเหตุของความบกพร่อง บนแท็บด่วน **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="f4495-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="f4495-114">คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="f4495-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="f4495-115">คลิกปุ่ม **จัดกลุ่มโดย** เพื่อแสดงระดับรายละเอียดที่จำเป็นต้องใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="f4495-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="f4495-116">ปุ่ม **จัดกลุ่มโดย** ที่เลือกจะถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="f4495-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="f4495-117">คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f4495-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="f4495-118">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f4495-118">Example</span></span>

<span data-ttu-id="f4495-119">ตัวอย่างนี้แสดงการคำนวณการควบคุมต้นทุนที่บกพร่องของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f4495-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="f4495-120">ฟิลด์ **งบประมาณเดิม** แสดงต้นทุนตามงบประมาณจากการคาดการณ์ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f4495-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="f4495-121">ฟิลด์ **ต้นทุนจริง** แสดงต้นทุนที่ลงรายการบัญชีบนใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f4495-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="f4495-122">ฟิลด์ **ต้นทุนผูกมัด** แสดงจำนวนรวมของต้นทุนที่บริษัทของคุณจะได้รับการกำหนดในความสัมพันธ์กับใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="f4495-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![รูปที่ 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="f4495-124">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าข้อบกพร่อง ดูที่หัวข้อ [การจัดการข้อบกพร่อง](../setup-for-work-orders/fault-management.md)</span><span class="sxs-lookup"><span data-stu-id="f4495-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]