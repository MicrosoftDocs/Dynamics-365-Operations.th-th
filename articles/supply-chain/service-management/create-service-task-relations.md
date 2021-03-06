---
title: การสร้างความสัมพันธ์ของภารกิจการให้บริการ
description: คุณสามารถเชื่อมโยงภารกิจการให้บริการกับข้อตกลงการให้บริการหรือใบสั่งบริการได้ เพื่ออธิบายภารกิจการให้บริการที่จะเสร็จสมบูรณ์สำหรับข้อตกลงหรือใบสั่ง
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e5fd978c1e9db7e7ce3c06bbeb45b59854f1582
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974671"
---
# <a name="create-service-task-relations"></a>การสร้างความสัมพันธ์ของภารกิจการให้บริการ    

[!include [banner](../includes/banner.md)]

คุณสามารถเชื่อมโยงภารกิจการให้บริการกับข้อตกลงการให้บริการหรือใบสั่งบริการได้ เพื่ออธิบายภารกิจการให้บริการที่จะเสร็จสมบูรณ์สำหรับข้อตกลงหรือใบสั่ง ข้อมูลนี้พร้อมใช้งานสำหรับช่างเทคนิคและลูกค้า

## <a name="create-a-relation-with-a-service-agreement"></a>สร้างความสัมพันธ์กับข้อตกลงการให้บริการ

1.  คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงการให้บริการ**

2.  เลือกข้อตกลงการให้บริการที่มีอยู่ หรือสร้างข้อตกลงการให้บริการใหม่

3.  บนบานหน้าต่างการดำเนินงาน คลิกปุ่ม **ภารกิจการให้บริการ**

4.  ในฟอร์ม **ภารกิจการให้บริการ** กด CTRL + N เพื่อสร้างรายการใหม่ และจากนั้น เลือกภารกิจการให้บริการจากรายการ **ภารกิจการให้บริการ** เพื่อแนบภารกิจการให้บริการกับข้อตกลงการให้บริการ

5.  บนแท็บ **คำอธิบาย** ป้อนคำอธิบายหมายเหตุภายในหรือภายนอกใดๆ ในฟิลด์ข้อความอิสระ

6.  ปิดแบบฟอร์มเพื่อบันทึกเรกคอร์ด

ทำขั้นตอนนี้ซ้ำจนกระทั่งคุณได้สร้างความสัมพันธ์ของภารกิจการให้บริการทั้งหมดที่จำเป็นสำหรับข้อตกลงการให้บริการ  ขณะนี้คุณสามารถระบุภารกิจการให้บริการเหล่านี้สำหรับบรรทัดข้อตกลงใดๆ ที่แนบได้

ความสัมพันธ์ของภารกิจการให้บริการที่สร้างในข้อตกลงการให้บริการสามารถใช้งานได้จากใบสั่งบริการทั้งหมดที่แนบกับข้อตกลงการให้บริการ

## <a name="create-a-relation-with-a-service-order"></a>สร้างความสัมพันธ์กับใบสั่งบริการ

1.  คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**

2.  เลือกใบสั่งบริการที่มีอยู่แล้ว หรือสร้างใบสั่งบริการใหม่

3.  บนบานหน้าต่างการดำเนินงาน คลิกปุ่ม **ภารกิจการให้บริการ**

4.  จากฟอร์ม **ภารกิจการให้บริการ** กด CTRL + N เพื่อสร้างรายการใหม่ และจากนั้น เลือกภารกิจการให้บริการจากรายการ **ภารกิจการให้บริการ** เพื่อแนบภารกิจการให้บริการกับข้อตกลงการให้บริการ

5.  บนแท็บ **คำอธิบาย** ป้อนคำอธิบายหมายเหตุภายในหรือภายนอกใดๆ ในฟิลด์ข้อความอิสระ

6.  ปิดแบบฟอร์มเพื่อบันทึกเรกคอร์ด

ทำขั้นตอนนี้ซ้ำจนกระทั่งคุณได้สร้างความสัมพันธ์ของภารกิจการให้บริการทั้งหมดที่จำเป็นสำหรับใบสั่งบริการ ขณะนี้คุณสามารถเลือกภารกิจการให้บริการที่คุณได้สร้างความสัมพันธ์ให้เมื่อคุณสร้างบรรทัดใบสั่งบริการ

ความสัมพันธ์ของภารกิจการให้บริการที่สร้างในใบสั่งบริการจะสามารถใช้งานได้ในใบสั่งบริการที่ระบุ

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ภาพรวมของงานบริการ](service-tasks.md)


  


