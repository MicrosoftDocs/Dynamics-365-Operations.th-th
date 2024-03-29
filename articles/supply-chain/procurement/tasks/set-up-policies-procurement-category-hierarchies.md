---
title: ตั้งค่านโยบายสำหรับการจัดประเภทการจัดซื้อตามลำดับชั้น
description: 'ใช้ขั้นตอนนี้เพื่อตั้งค่ากฎสำหรับการเรียงลำดับผลิตภัณฑ์ในประเภท '
author: GalynaFedorova
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2a8248374f34e0937aa569259c5925506857ddd
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675920"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>ตั้งค่านโยบายสำหรับการจัดประเภทการจัดซื้อตามลำดับชั้น

[!include [banner](../../includes/banner.md)]

ใช้ขั้นตอนนี้เพื่อตั้งค่ากฎสำหรับการเรียงลำดับผลิตภัณฑ์ในประเภท  มีการกำหนดกฎสำหรับนโยบายการจัดซื้อเฉพาะ กฎการเข้าถึงประเภทควบคุมประเภทการจัดซื้อที่พนักงานมีสิทธิเข้าถึงเมื่อสร้างใบสั่ง เมื่อมีการสร้างใบสั่ง นโยบายการจัดซื้อและกฎการเข้าถึงประเภทที่ควรใช้จะขึ้นอยู่กับนิติบุคคลและหน่วยปฏิบัติงานที่พนักงานเป็นสมาชิก คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF โดยทั่วไปงานนี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ


## <a name="find-the-procurement-policy"></a>ค้นหานโยบายการจัดซื้อ
1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > การตั้งค่า > นโยบาย > นโยบายการจัดซื้อ**
2. คลิกลิงค์ในนโยบาย 'นโยบายการจัดซื้อ USMF' นี่คือนโยบายที่คุณจะเพิ่มกฎเข้าไป ซึ่งต้องเป็นนโยบายที่ใช้งานอยู่  

## <a name="create-a-category-access-rule"></a>สร้างกฎการเข้าถึงประเภท
1. ขยาย fastTab **กฎนโยบาย**
2. ในรายการ **ชนิดของกฎนโยบาย** เลือก **กฎนโยบายการเข้าถึงประเภท** ถ้าปุ่ม **สร้างกฎนโยบาย** เป็นสีเทา นั่นเป็นเพราะมีกฎนโยบายที่ใช้งานอยู่สำหรับการเข้าถึงประเภทแล้ว ตรวจสอบฟิลด์ **มีผลบังคับใช้** และฟิลด์ **การหมดอายุ** เพื่อกำหนด จากนั้นเลือก และคลิก **ถอนกฎนโยบาย** ถ้าปุ่ม **สร้างกฎนโยบาย** พร้อมใช้งาน คุณไม่จำเป็นต้องทำสิ่งใด  
3. คลิก **สร้างกฎนโยบาย**
4. ในฟิลด์ **วันที่มีผลบังคับใช้** ป้อนวันที่และเวลา เวลาจะต้องไม่ทับซ้อนกับกฎอื่นที่ใช้งานอยู่แล้ว  
5. เลือกประเภทที่จะใช้กฎ  จดบันทึกว่านี่คือประเภทใด – คุณจะต้องใช้ในภายหลัง เมื่อคุณเลือกประเภทแล้ว ประเภทหลักหรือประเภทต่าง ๆ จะถูกเพิ่มเข้าในรายการประเภทที่เลือก หากคุณต้องการใช้กฎกับประเภทย่อยทั้งหมดของประเภทที่เลือก ให้เลือกกล่องกาเครื่องหมาย **รวมประเภทย่อย**
6. คลิกลูกศรทางขวาเพื่อเพิ่มลงในรายการ **ประเภทที่เลือก**  
4. คลิก **ตกลง** หากคุณตั้งค่าตัวเลือก **รวมกฎหลัก** เป็น ใช่ กฎนโยบายที่คุณกำหนดสำหรับประเภทหลักยังจะถูกกำหนดให้กับประเภทรองด้วย หากไม่มีการกำหนดกฎนโยบายให้แก่ประเภทรอง

## <a name="create-a-category-policy-rule"></a>สร้างกฎนโยบายประเภท
1. ในรายการ **ชนิดของกฎนโยบาย** เลือก **กฎนโยบายประเภท** ถ้าปุ่ม **สร้างกฎนโยบายเป็นสีเทา** ให้เลือกกฎนโยบายที่ใช้งานอยู่ และจากนั้นคลิก **ถอนกฎนโยบาย**  
2. คลิก **สร้างกฎนโยบาย**
3. ในฟิลด์ **วันที่มีผลบังคับใช้** ป้อนวันที่และเวลา
4. คลิก **เพิ่ม**
5. ในฟิลด์ **ประเภท** เลือกประเภทเดียวกันกับที่คุณใช้สำหรับ **กฎการเข้าถึงประเภท**
6. ในฟิลด์ **การเลือกผู้จัดจำหน่าย** ให้เลือกหนึ่งตัวเลือก เลือกกฎที่จะควบคุมชนิดของผู้จัดจำหน่ายที่สามารถเลือกสำหรับประเภทเมื่อมีการสร้างใบขอซื้อ  
7. คลิก **ปิด** กฎนโยบายที่คุณได้กำหนดไว้มีไว้สำหรับใบขอซื้อชนิดของปริมาณการใช้วัสดุ  ถ้าคุณต้องการกำหนดนโยบายสำหรับใบขอซื้อของชนิดการเติมสินค้า คุณต้องสร้างกฎสำหรับชนิดกฎนโยบายที่เรียกว่า "กฎนโยบายการเข้าถึงประเภทการเติมสินค้า"  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]