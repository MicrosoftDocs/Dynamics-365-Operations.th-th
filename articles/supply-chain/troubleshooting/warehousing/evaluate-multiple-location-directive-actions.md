---
title: ประเมินการดำเนินการทั้งหมดสำหรับคำสั่งสถานที่ตั้งแบบหลาย SKU
description: ลักษณะการทำงานใหม่ถูกเพิ่มเพื่อประเมินการดำเนินการทั้งหมดสำหรับคำสั่งที่ตั้งหลาย SKU หน้านี้จะแนะนำให้คุณเห็นถึงข้อมูลเกี่ยวกับวิธีการเปิด
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2d5f7cf548eb6c18d9700c73ef084f197b78542e
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102974"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>ตัวเลือก SKU หลายรายการไม่ได้ประเมินหลายการดำเนินคำสั่งสถานที่

## <a name="symptoms"></a>อาการ

คำสั่งสถานที่ของชนิดใบสั่งงาน *ใบสั่งขาย* และชนิดงาน *สำรอง* ไม่ประเมินการดำเนินการคำสั่งของสถานที่ต่าง ๆ เมื่อตัวเลือก **หลาย SKU** ถูกเลือก มีการประเมินเฉพาะการดำเนินการคำสั่งสถานที่แรกเท่านั้น

## <a name="resolution"></a>การแก้ปัญหา

ลักษณะการทำงานใหม่ *ประเมินการดำเนินการทั้งหมดสำหรับคำสั่งที่ตั้งหลาย SKU* ซึ่งถูกเพิ่มเข้าในรุ่น 10.0.15 (โปรดดูที่ [4579866 KB](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)) ลักษณะการทำงานนี้จะประเมินการดำเนินการทั้งหมดสำหรับคำสั่งที่ตั้งหลาย SKU (เริ่มจาก Supply Chain Management เวอร์ชัน 10.0.21 คุณลักษณะนี้จะเปิดตามค่าเริ่มต้น)  เริ่มจาก Supply Chain Management รุ่น 10.0.25 คุณลักษณะนี้เป็นแบบบังคับและไม่สามารถปิดได้ ผู้ดูแลระบบสามารถใช้หน้า [การจัดการคุณลักษณะ](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดหรือปิดการใช้งานได้ถ้าจำเป็น
