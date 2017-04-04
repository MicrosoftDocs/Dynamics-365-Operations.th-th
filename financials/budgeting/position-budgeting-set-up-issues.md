---
title: "ตำแหน่งที่มีการแก้ไขปัญหาการจัดงบประมาณ"
description: "บทความนี้ให้คำตอบแก่คำถามที่คุณอาจมี เมื่อคุณตั้งค่าคอนฟิกการจัดทำงบประมาณของตำแหน่ง  จะเน้นคำถามที่ถูกถามบ่อยเกี่ยวกับวิธีการสร้างองค์ประกอบต้นทุนงบประมาณ กลุ่มค่าตอบแทน และกริดค่าตอบแทน"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 8d4025e805545cc518f90f8dc4786fd61d8f6d93
ms.lasthandoff: 03/31/2017


---

# <a name="position-budgeting-troubleshooting"></a>ตำแหน่งที่มีการแก้ไขปัญหาการจัดงบประมาณ

บทความนี้ให้คำตอบแก่คำถามที่คุณอาจมี เมื่อคุณตั้งค่าคอนฟิกการจัดทำงบประมาณของตำแหน่ง  จะเน้นคำถามที่ถูกถามบ่อยเกี่ยวกับวิธีการสร้างองค์ประกอบต้นทุนงบประมาณ กลุ่มค่าตอบแทน และกริดค่าตอบแทน 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>เหตุใดฉันจึงไม่พบหน้าตำแหน่งการคาดการณ์ในทรัพยากรบุคคล
---------------------------------------------------------------

มีการย้ายตำแหน่งตามการคาดการณ์การจัดทำงบประมาณ

## <a name="why-cant-i-delete-a-budget-cost-element"></a>เหตุใดฉันจึงไม่สามารถลบองค์ประกอบต้นทุนงบประมาณการ
คุณไม่สามารถลบองค์ประกอบต้นทุนงบประมาณที่กำหนดให้กับตำแหน่งตามการคาดการณ์  ก่อนที่คุณสามารถลบออกองค์ประกอบต้นทุนงบประมาณ คุณต้องลบออกจากตำแหน่งตามการคาดการณ์ทั้งหมดก่อน **เคล็ดลับ:**เมื่อต้องการค้นหาทุก ตำแหน่งองค์ประกอบต้นทุนงบประมาณกำหนดให้กับ เลือกองค์ประกอบต้นทุนในการ**งบประมาณต้นทุนองค์ประกอบ**หน้า และจากนั้น คลิ**ปรับปรุงตำแหน่ง** ตำแหน่งที่ใช้องค์ประกอบต้นทุนถูกแสดงรายการอยู่ในกริดด้านบน

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>ฉันสามารถลบเป็นองค์ประกอบต้นทุนจากตำแหน่งตามการคาดการณ์หลายรายการโดยไม่ต้องเปิดแต่ละรายการได้อย่างไร
คุณไม่สามารถลบองค์ประกอบต้นทุนได้  อย่างไรก็ตาม ถ้าคุณเปลี่ยนวันที่เริ่มต้นและสิ้นสุด เพื่อให้อยู่นอกวันที่วงจรการวางแผนงบประมาณ องค์ประกอบต้นทุนจะไม่ถูกกำหนดให้กับตำแหน่งตามการคาดการณ์ในวงจรการวางแผนงบประมาณอีกต่อไป  To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date. Then click **OK** to automatically update all forecast positions that the cost element is assigned to. **เคล็ดลับ:**ถ้าคุณใช้วิธีนี้ โปรดทราบว่า จะเอาองค์ประกอบต้นทุนงบประมาณจาก**ทั้งหมด**ตำแหน่งตามการคาดการณ์ที่วันที่เริ่มต้นและสิ้นสุดจะไม่อยู่ในช่วงที่เหมาะสม ถ้าผลกระทบนี้ไม่ใช่สิ่งที่คุณต้องการ คุณต้องเปิดตำแหน่งตามการคาดการณ์แต่ละแห่งที่คุณต้องการลบองค์ประกอบต้นทุนงบประมาณ และทำการเปลี่ยนแปลงด้วยตนเอง

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>เหตุใดฉันจึงไม่สามารถป้อนยอดเงินประจำปีใน FastTab การคำนวณต้นทุนสำหรับองค์ประกอบต้นทุนงบประมาณได้
You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value. To change the value, remove all budget cost elements from the **Calculation basis** FastTab.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>เหตุใดฉันจึงไม่สามารถเปลี่ยนชนิดของต้นทุนงบประมาณจาก รายได้ เป็นชนิดต้นทุนงบประมาณอื่น
บางองค์ประกอบต้นทุนงบประมาณใช้องค์ประกอบต้นทุนของรายได้เป็นพื้นฐานการคำนวณ  To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>เพราะไม่สามารถเปลี่ยนวันที่ในรายการองค์ประกอบต้นทุนงบประมาณสำหรับองค์ประกอบต้นทุนงบประมาณ
คุณไม่สามารถเปลี่ยนวันที่ในรายการองค์ประกอบต้นทุนงบประมาณได้ เมื่อองค์ประกอบต้นทุนงบประมาณถูกใช้โดยตำแหน่งตามการคาดการณ์  การจำกัดนี้ช่วยรับรองว่าตำแหน่งตามการคาดการณ์อยู่ภายในคำแนะนำขององค์ประกอบต้นทุนงบประมาณเสมอ  To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates. Then click **OK** to update the positions that the cost element is assigned to.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>เหตุใดฉันจึงไม่สามารถเปลี่ยนต้นทุนสำหรับองค์ประกอบต้นทุนงบประมาณบนหน้ากลุ่มค่าตอบแทนได้
คุณสามารถสร้างและเปลี่ยนแปลงองค์ประกอบต้นทุนงบประมาณเท่านั้น ในหน้า **องค์ประกอบต้นทุนงบประมาณ** ได้

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>เหตุใดฉันจึงได้รับข้อความแสดงข้อผิดพลาด เมื่อฉันเปลี่ยนแปลงวันที่สำหรับองค์ประกอบต้นทุนในตำแหน่งตามการคาดการณ์
วันที่บนรายการองค์ประกอบต้นทุนของตำแหน่งการคาดการณ์ต้องอยู่ภายในช่วงต่อไปนี้:

-   วันเปิดใช้งานและพ้นจากตำแหน่ง
-   วันเปิดใช้งานและหมดอายุขององค์ประกอบต้นทุนงบประมาณ
-   วันที่เริ่มต้นและสิ้นสุดของวงจรงบประมาณ ที่เชื่อมโยงกับกระบวนการการวางแผนงบประมาณของตำแหน่งตามการคาดการณ์



