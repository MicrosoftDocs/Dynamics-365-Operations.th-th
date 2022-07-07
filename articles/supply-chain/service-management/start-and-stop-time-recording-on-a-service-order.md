---
title: การเริ่มต้นและหยุดการบันทึกเวลาของใบสั่งบริการ
description: เริ่มต้นและหยุดการบันทึกเวลาของใบสั่งบริการ
author: sorenva
ms.date: 05/07/2018
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
ms.openlocfilehash: 7b110c6a08d946b4527f47f6d4181819f3508fee
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016346"
---
# <a name="start-and-stop-time-recording-on-a-service-order"></a>การเริ่มต้นและหยุดการบันทึกเวลาของใบสั่งบริการ 

[!include [banner](../includes/banner.md)]


ใช้ขั้นตอนนี้เพื่อเริ่มต้น และหยุดการบันทึกเวลาสำหรับใบสั่งบริการที่มีกำหนดข้อตกลงระดับการให้บริการ

## <a name="start-time-recording"></a>เริ่มการจัดทำเรกคอร์ดเวลา

1.  คลิก **การจัดการบริการ** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**

2.  คลิกแท็บ **ใบสั่งบริการ** บน **บานหน้าต่างการดำเนินการ** ในกลุ่ม **ข้อตกลงระดับการบริการ** คลิก **เริ่มต้น**

3.  ป้อนวันที่และเวลาที่ควรเริ่มต้นการบันทึกเวลา

## <a name="stop-time-recording"></a>หยุดการจัดทำเรกคอร์ดเวลา

1.  คลิก **การจัดการบริการ** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**

2.  คลิกแท็บ **ใบสั่งบริการ** บน **บานหน้าต่างการดำเนินการ** ในกลุ่ม **ข้อตกลงระดับการบริการ** คลิก **หยุด**

3.  ป้อนวันที่และเวลาที่ควรหยุดการจัดทำเรกคอร์ดเวลา

4.  เลือก **เพิ่มเหตุผลการเพิกถอน** และเลือกรหัสเหตุผลในรายการ **รหัสเหตุผลของขั้นตอน** เพื่อระบุเหตุผลในการหยุดการบันทึกเวลา


> [!NOTE]
> <P>ถ้า <STRONG>รหัสเหตุผลที่เกินเวลา</STRONG> ถูกเลือกไว้ในแบบฟอร์ม <STRONG>พารามิเตอร์การจัดการบริการ</STRONG> คุณต้องระบุรหัสเหตุผล ก่อนที่คุณจะสามารถหยุดการบันทึกเวลาได้</P>



## <a name="see-also"></a>ดูเพิ่มเติมที่

[การเริ่มต้นการจัดทำเรกคอร์ดเวลา SLA (แบบฟอร์ม)](https://technet.microsoft.com/library/hh242297\(v=ax.60\))

[หยุดการจัดทำเรกคอร์ดเวลา SLA (แบบฟอร์ม)](https://technet.microsoft.com/library/hh242241\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]