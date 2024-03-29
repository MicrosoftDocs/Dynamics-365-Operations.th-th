---
title: ยกเลิกใบสั่งบริการ
description: คุณสามารถยกเลิกใบสั่งบริการหรือรายการใบสั่งบริการได้จากตัวใบสั่งบริการเอง หรือคุณสามารถยกเลิกใบสั่งบริการหลายใบได้โดยการรันงานประจำงวด
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 228b76d6f6f0bb048662c8e82df76f51b7cb3652
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017389"
---
# <a name="cancel-service-orders"></a>ยกเลิกใบสั่งบริการ   

[!include [banner](../includes/banner.md)]


คุณสามารถยกเลิกใบสั่งบริการหรือรายการใบสั่งบริการได้จากตัวใบสั่งบริการเอง หรือคุณสามารถยกเลิกใบสั่งบริการหลายใบได้โดยการรันงานประจำงวด


> [!NOTE]
> <P>ใบสั่งบริการไม่สามารถยกเลิกได้ ถ้าขั้นตอนของใบสั่งบริการไม่อนุญาตการยกเลิก ถ้าใบสั่งบริการมีความต้องการสินค้า หรือถ้าใบสั่งบริการได้ถูกลงรายการบัญชีแล้ว</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>การยกเลิกใบสั่งบริการในแบบฟอร์มใบสั่งบริการ

1.  คลิก **การจัดการบริการ** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ** เลือกใบสั่งบริการ และในบานหน้าต่างการดำเนินการ คลิก **ยกเลิกใบสั่ง**

## <a name="cancel-a-service-order-line"></a>การยกเลิกบรรทัดใบสั่งบริการ

1.  คลิก **การจัดการบริการ** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ** ดับเบิลคลิกใบสั่งบริการที่ประกอบด้วยรายการที่คุณต้องการยกเลิก

2.  เลือกรายการใบสั่งบริการที่คุณต้องการยกเลิก แล้วคลิก **ยกเลิกรายการใบสั่ง** เพื่อเปลี่ยนสถานะของรายการเป็น **ถูกยกเลิกแล้ว**


> [!TIP]
> <P>ในการกลับรายการการยกเลิกของรายการใบสั่งบริการ และเปลี่ยนสถานะกลับไปเป็น <STRONG>สร้างแล้ว</STRONG> คลิก <STRONG>ถอนการยกเลิก</STRONG></P>


## <a name="cancel-multiple-service-orders"></a>การยกเลิกใบสั่งบริการหลายใบ

1.  คลิก **การจัดการบริการ** \> **งานประจำงวด** \> **ใบสั่งบริการ** \> **ยกเลิกใบสั่งบริการ**

2.  คลิกปุ่ม **เลือก** 

3.  ในแบบฟอร์ม **การสอบถาม** ในคอลัมน์ **เงื่อนไข** เลือกใบสั่งบริการที่คุณต้องการยกเลิก

4.  คลิก **ตกลง** เพื่อปิดแบบฟอร์ม **การสอบถาม**

5.  เลือกกล่องกาเครื่องหมาย **แสดง Infolog** เพื่อสร้าง Infolog ซึ่งแสดงใบสั่งบริการที่ยกเลิกแล้ว

6.  เลือกกล่องกาเครื่องหมาย **เพิกถอนการยกเลิก** ถ้าคุณต้องการกลับรายการสถานะ **ยกเลิกแล้ว** ของใบสั่งบริการ

7.  คลิก **ตกลง** 

ใบสั่งบริการที่เลือกไว้จะถูกยกเลิก หรือสถานะความคืบหน้า **ยกเลิกแล้ว** ถูกกลับรายการเป็น **อยู่ระหว่างดำเนินการ**


> [!NOTE]
> <P>ถ้าคุณเลือกกล่องกาเครื่องหมาย <STRONG>เพิกถอนการยกเลิก</STRONG> ใบสั่งบริการที่มีสถานะความคืบหน้าเป็น <STRONG>ยกเลิกแล้ว</STRONG> จะถูกกลับรายการ และไม่มีการยกเลิกใบสั่งบริการที่มีสถานะความคืบหน้าเป็น <STRONG>อยู่ระหว่างดำเนินการ</STRONG></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]