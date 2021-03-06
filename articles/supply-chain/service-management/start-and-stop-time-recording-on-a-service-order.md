---
title: การเริ่มต้นและหยุดการบันทึกเวลาของใบสั่งบริการ
description: เริ่มต้นและหยุดการบันทึกเวลาของใบสั่งบริการ
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0ce68881e7b39fac314e3bafe022e30a10dcbe2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991625"
---
# <a name="start-and-stop-time-recording-on-a-service-order"></a>การเริ่มต้นและหยุดการบันทึกเวลาของใบสั่งบริการ 

[!include [banner](../includes/banner.md)]


ใช้ขั้นตอนนี้เพื่อเริ่มต้น และหยุดการบันทึกเวลาสำหรับใบสั่งบริการที่มีกำหนดข้อตกลงระดับการให้บริการ

## <a name="start-time-recording"></a>เริ่มการจัดทำเรกคอร์ดเวลา

1.  คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**

2.  คลิกแท็บ **ใบสั่งบริการ** บน **บานหน้าต่างการดำเนินการ** ในกลุ่ม **ข้อตกลงระดับการบริการ** คลิก **เริ่มต้น**

3.  ป้อนวันที่และเวลาที่ควรเริ่มต้นการบันทึกเวลา

## <a name="stop-time-recording"></a>หยุดการจัดทำเรกคอร์ดเวลา

1.  คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**

2.  คลิกแท็บ **ใบสั่งบริการ** บน **บานหน้าต่างการดำเนินการ** ในกลุ่ม **ข้อตกลงระดับการบริการ** คลิก **หยุด**

3.  ป้อนวันที่และเวลาที่ควรหยุดการจัดทำเรกคอร์ดเวลา

4.  เลือก **เพิ่มเหตุผลการเพิกถอน** และเลือกรหัสเหตุผลในรายการ **รหัสเหตุผลของขั้นตอน** เพื่อระบุเหตุผลในการหยุดการบันทึกเวลา


> [!NOTE]
> <P>ถ้า <STRONG>รหัสเหตุผลที่เกินเวลา</STRONG> ถูกเลือกไว้ในแบบฟอร์ม <STRONG>พารามิเตอร์การจัดการบริการ</STRONG> คุณต้องระบุรหัสเหตุผล ก่อนที่คุณจะสามารถหยุดการบันทึกเวลาได้</P>



## <a name="see-also"></a>ดูเพิ่มเติมที่

[การเริ่มต้นการจัดทำเรกคอร์ดเวลา SLA (แบบฟอร์ม)](https://technet.microsoft.com/library/hh242297\(v=ax.60\))

[หยุดการจัดทำเรกคอร์ดเวลา SLA (แบบฟอร์ม)](https://technet.microsoft.com/library/hh242241\(v=ax.60\))

  


