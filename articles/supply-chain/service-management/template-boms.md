---
title: "BOM เท็มเพลต"
description: "สูตรการผลิตของเท็มเพลต (BOM) ให้รายการของส่วนประกอบที่เป็นมาตรฐานสำหรับวัตถุที่ให้บริการที่มีการให้บริการอย่างสม่ำเสมอ"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6e3a16b9938f6d4222e0a95078356f457e71a1bb
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="template-boms"></a><span data-ttu-id="4f5a7-103">BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="4f5a7-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4f5a7-104">สูตรการผลิตของเท็มเพลต (BOM) ให้คุณมีรายการของส่วนประกอบที่เป็นมาตรฐานสำหรับวัตถุที่ให้บริการที่มีการให้บริการอย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="4f5a7-105">ส่วนประกอบที่แสดงรายการอยู่ใน BOM เท็มเพลต แสดงถึงส่วนประกอบย่อยแต่ละรายการของวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="4f5a7-106">โดยการใช้ BOM เท็มเพลตกับวัตถุที่ให้บริการ คุณจะสามารถเก็บเรกคอร์ดของส่วนประกอบย่อยที่ได้มีการเปลี่ยนในวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="4f5a7-107">ถ้าต้องการใช้ BOM เท็มเพลตกับข้อตกลงการให้บริการหรือใบสั่งบริการ คุณสามารถแนบ BOM เท็มเพลตกับความสัมพันธ์ของวัตถุที่ให้บริการได้</span><span class="sxs-lookup"><span data-stu-id="4f5a7-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4f5a7-108">คุณสามารถใช้ BOM เท็มเพลตได้เพียงหนึ่งรายการเท่านั้นกับวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="4f5a7-109">การสร้าง BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="4f5a7-109">Create a template BOM</span></span>

<span data-ttu-id="4f5a7-110">ตารางต่อไปนี้ประกอบด้วยข้อมูลเกี่ยวกับวิธีการต่างๆ ที่คุณสามารถใช้เพื่อสร้าง BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="4f5a7-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f5a7-111">วิธีการ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-111">Method</span></span></p></th>
<th><p><span data-ttu-id="4f5a7-112">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4f5a7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f5a7-113">การผลิต</span><span class="sxs-lookup"><span data-stu-id="4f5a7-113">Production</span></span></p></td>
<td><p><span data-ttu-id="4f5a7-114">BOM เท็มเพลตยึดตามใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="4f5a7-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="4f5a7-115">ตัวเลือกนี้จะใช้ได้ ก็ต่อเมื่อคุณดำเนินงานในสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="4f5a7-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="4f5a7-116">ข้อดีของวิธีการนี้คือคุณจะมีรายการที่เป็นปัจจุบันและละเอียดของส่วนประกอบต่างๆ ที่ประกอบขึ้นเป็นสินค้า</span><span class="sxs-lookup"><span data-stu-id="4f5a7-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f5a7-117">สินค้า BOM</span><span class="sxs-lookup"><span data-stu-id="4f5a7-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="4f5a7-118">BOM เท็มเพลตยึดตาม BOM สินค้า</span><span class="sxs-lookup"><span data-stu-id="4f5a7-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="4f5a7-119">BOM สินค้า ซึ่งไม่เหมือนกับ BOM การผลิต เป็นรายการแบบคงที่ของส่วนประกอบที่ประกอบขึ้นเป็นสินค้า</span><span class="sxs-lookup"><span data-stu-id="4f5a7-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f5a7-120">เท็มเพลตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4f5a7-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="4f5a7-121">เท็มเพลตยึดตาม BOM เท็มเพลตที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4f5a7-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f5a7-122">ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="4f5a7-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="4f5a7-123">หากคุณทราบว่าอะไหล่สำรองใดมักจะถูกเปลี่ยนในวัตถุที่ให้บริการ คุณสามารถสร้าง BOM เท็มเพลตของคุณด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="4f5a7-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="4f5a7-124">วิธีการนี้ช่วยทำให้แน่ใจได้ว่า ส่วนประกอบต่างๆ ที่ถูกรวมไว้ในเท็มเพลตจะสะท้อนถึงความต้องการที่แท้จริงของสถานที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="4f5a7-125">นำ BOM เท็มเพลตไปใช้กับข้อตกลงการให้บริการ หรือใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="4f5a7-126">คุณสามารถนำ BOM เท็มเพลตไปใช้กับข้อตกลงการให้บริการ ใบสั่งบริการ หรือทั้งสองรายการได้</span><span class="sxs-lookup"><span data-stu-id="4f5a7-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="4f5a7-127">โดยปกติแล้ว ข้อตกลงการให้บริการครอบคลุมความสัมพันธ์กับลูกค้าในระยะยาว </span><span class="sxs-lookup"><span data-stu-id="4f5a7-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="4f5a7-128">ประวัติของการเปลี่ยนที่บันทึกไว้ใน BOM การบริการ เป็นข้อมูลที่มีประโยชน์ที่ควรมีสำหรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="4f5a7-129">คุณยังสามารถใช้ BOM เท็มเพลตกับใบสั่งบริการ เพื่อบันทึกประวัติของการบริการที่ได้มีการดำเนินการในวัตถุที่ให้บริการได้</span><span class="sxs-lookup"><span data-stu-id="4f5a7-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="4f5a7-130">คัดลอกประวัติของ BOM การบริการ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="4f5a7-131">คุณสามารถคัดลอกประวัติของรายการ BOM การบริการจากข้อตกลงการให้บริการหนึ่งไปยังข้อตกลงการให้บริการอื่นได้</span><span class="sxs-lookup"><span data-stu-id="4f5a7-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="4f5a7-132">โดยการคัดลอกประวัติการบริการระหว่างข้อตกลงการให้บริการต่างๆ คุณจึงสามารถเก็บรักษาเรกคอร์ดของการเปลี่ยนสำหรับสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="4f5a7-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="4f5a7-133">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="4f5a7-133">**Example**</span></span>

<span data-ttu-id="4f5a7-134">คุณได้ตั้งค่าข้อตกลงการให้บริการระยะเวลาสามปีสำหรับรถยนต์ของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="4f5a7-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="4f5a7-135">ในระหว่างรอบระยะเวลานั้น ลูกค้าจะรู้สึกคุ้นเคยกับการบริการดีที่บริษัทนำเสนอ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="4f5a7-136">ดังนั้น หลังจากที่ข้อตกลงหมดอายุ ลูกค้าต้องการตั้งค่ารายการใหม่</span><span class="sxs-lookup"><span data-stu-id="4f5a7-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="4f5a7-137">ขณะนี้คุณสามารถเจรจาต่อรองข้อตกลงที่บริษัทได้รับประโยชน์มากขึ้นได้ </span><span class="sxs-lookup"><span data-stu-id="4f5a7-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="4f5a7-138">เนื่องจากเรกคอร์ดของส่วนประกอบที่เปลี่ยนอาจเป็นประโยชน์ในอนาคต คุณจึงคัดลอกประวัติของ BOM การบริการไปยังข้อตกลงฉบับใหม่</span><span class="sxs-lookup"><span data-stu-id="4f5a7-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="4f5a7-139">ปรับเปลี่ยน BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="4f5a7-139">Modify the template BOM</span></span>

<span data-ttu-id="4f5a7-140">ถ้ายังไม่ได้แนบ BOM เท็มเพลตกับวัตถุที่ให้บริการ คุณสามารถปรับเปลี่ยนหรือลบรายการในนั้นได้</span><span class="sxs-lookup"><span data-stu-id="4f5a7-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="4f5a7-141">หลังจากที่แนบ BOM เท็มเพลตกับวัตถุที่ให้บริการแล้ว คุณสามารถปรับเปลี่ยนได้เฉพาะเวอร์ชันเฉพาะที่ของ BOM เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4f5a7-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="4f5a7-142">ถ้าคุณต้องการทำซ้ำการตั้งค่าของเวอร์ชันเฉพาะที่ของ BOM เท็มเพลต คุณสามารถสร้าง BOM เท็มเพลตขึ้นใหม่ตามข้อมูลเวอร์ชันเฉพาะที่ได้ </span><span class="sxs-lookup"><span data-stu-id="4f5a7-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="4f5a7-143">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [แก้ไข BOM การบริการ](modify-service-bom.md)</span><span class="sxs-lookup"><span data-stu-id="4f5a7-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="4f5a7-144">ถ้าคุณเปลี่ยนสินค้าใน BOM คุณสามารถลงทะเบียนการเปลี่ยนนั้นได้ในรายการ BOM ในตัวออกแบบ BOM</span><span class="sxs-lookup"><span data-stu-id="4f5a7-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="4f5a7-145">คุณสามารถเลือกที่จะสร้างรายการใบสั่งบริการสำหรับวัตถุที่เปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="4f5a7-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="4f5a7-146">ถ้าคุณสร้างรายการใบสั่งบริการ คุณสามารถออกใบแจ้งหนี้สินค้าที่เปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="4f5a7-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="4f5a7-147">ถ้าคุณไม่ได้สร้างรายการใบสั่งบริการสำหรับการเปลี่ยน ระบบจะเก็บรักษาการลงทะเบียนการเปลี่ยนนั้นไว้ เพื่อใช้ในการติดตามประวัติของวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="4f5a7-148">เปลี่ยนวิธีการแสดงข้อมูลบนรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="4f5a7-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="4f5a7-149">คุณสามารถเปลี่ยนวิธีที่ข้อมูลในรายการ BOM ถูกแสดง สำหรับ BOM เท็มเพลตและ BOM การบริการทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="4f5a7-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="4f5a7-150">การเปลี่ยนแปลงถูกนำไปใช้กับ BOM เท็มเพลตและ BOM การบริการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4f5a7-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="4f5a7-151">ซึ่งรวมถึงรายการเหล่านั้นที่แนบกับวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="4f5a7-152">ตั้งค่าลำดับหมายเลขสำหรับ BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="4f5a7-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="4f5a7-153">ในการใช้ BOM เท็มเพลต คุณต้องตั้งค่าลำดับหมายเลขสองลำดับ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="4f5a7-154">ตั้งค่าลำดับหมายเลขหนึ่งลำดับสำหรับ BOM เท็มเพลต และอีกหนึ่งลำดับสำหรับหมายเลขรายการประวัติ BOM</span><span class="sxs-lookup"><span data-stu-id="4f5a7-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4f5a7-155">มีการใช้ลำดับหมายเลขทั่วทั้ง Microsoft Dynamics AX เพื่อปันส่วนตัวระบุให้กับเรกคอร์ดที่ต้องการรายการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="4f5a7-155">Number sequences are used throughout Microsoft Dynamics AX to allocate identifiers to records that require them.</span></span> <span data-ttu-id="4f5a7-156">ก่อนที่คุณจะสามารถกำหนดลำดับหมายเลขให้กับ BOM เท็มเพลตหรือหมายเลขรายการประวัติ BOM ได้ คุณต้องตั้งค่ารหัสลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="4f5a7-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="4f5a7-157">ตั้งค่าลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="4f5a7-157">Set up number sequences</span></span>

1.  <span data-ttu-id="4f5a7-158">ในหน้ารายการ **ลำดับหมายเลข** สร้างลำดับหมายเลข สำหรับ BOMs เท็มเพลตและหมายเลขรายการประวัติ BOM</span><span class="sxs-lookup"><span data-stu-id="4f5a7-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="4f5a7-159">คลิก **การจัดการงานบริการ** \> **ตั้งค่า** \> **พารามิเตอร์การจัดการงานบริการ**</span><span class="sxs-lookup"><span data-stu-id="4f5a7-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="4f5a7-160">คลิก **ลำดับหมายเลข** และจากนั้นเลือกรหัสลำดับหมายเลขสำหรับการอ้างอิงลำดับหมายเลขที่คุณสร้างขึ้นในแบบฟอร์ม **ลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="4f5a7-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="4f5a7-161">ปิดแบบฟอร์มเพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4f5a7-162">หมายเลขรายการประวัติ BOM ถูกใช้โดยระบบ เพื่อเชื่อมโยงธุรกรรมในประวัติ BOM กับข้อตกลงการให้บริการหรือใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="4f5a7-163">หมายเลขจะไม่แสดงขึ้นในอินเทอร์เฟสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="4f5a7-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="4f5a7-164">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="4f5a7-164">See also</span></span>

[<span data-ttu-id="4f5a7-165">การสร้าง BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="4f5a7-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="4f5a7-166">การจัดการ BOM เท็มเพลตสำหรับความสัมพันธ์ของออบเจ็กต์</span><span class="sxs-lookup"><span data-stu-id="4f5a7-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="4f5a7-167">การแก้ไข BOM การบริการ</span><span class="sxs-lookup"><span data-stu-id="4f5a7-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 



