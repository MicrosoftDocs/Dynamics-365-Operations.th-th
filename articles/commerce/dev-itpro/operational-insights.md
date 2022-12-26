---
title: ตั้งค่า Operational Insights
description: บทความนี้จะอธิบายวิธีการตั้งค่าและใช้งานคุณลักษณะ Operational Insights ใน Microsoft Dynamics 365 Commerce
author: ashishMSFT
ms.date: 12/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ca0d31e403275d6131fa6d53f0a7b46a7ddb651d
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832143"
---
# <a name="set-up-operational-insights"></a>ตั้งค่า Operational Insights

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการตั้งค่าและใช้งานคุณลักษณะ Operational Insights ใน Microsoft Dynamics 365 Commerce

Operational Insights คือคุณลักษณะ Dynamics 365 Commerce ที่ออกแบบมาเพื่อให้มองเห็นได้ดีขึ้นเกี่ยวกับสุขภาพการบริการและฟังก์ชันทางธุรกิจของลูกค้า โดยการส่งเทเลเมตรี่ไปยังบัญชีที่ลูกค้า Application Insights เป็นเจ้าของโดยตรง

โดยการเปิดใช้งาน Operational Insights สำหรับสภาพแวดล้อมของคุณใน Commerce headquarters คุณสามารถรวบรวมรายการเหตุการณ์ที่สัญลักษณ์จากทั้ง Commerce Scale Unit (CSU) และอุปกรณ์จุดขาย (POS) ของคุณ เหตุการณ์เหล่านี้ช่วยให้คุณเข้าใจวิธีการปฏิบัติงานของระบบของคุณได้ดียิ่งขึ้น และช่วยให้คุณสามารถตรวจสอบเมตริกทางเทคนิคและธุรกิจหลักได้

แม้ว่าคุณจะไม่ต้องการรวบรวมเทเลเมรี่นี้ตลอดเวลา แต่คุณจะสามารถได้รับประโยชน์จากการเปิดใช้งานหรือปิดใช้งานการเรียกเก็บเงินอย่างรวดเร็วในสภาพแวดล้อมเฉพาะ ด้วยวิธีนี้ เทเลเมต์สามารถช่วยคุณในการแก้ไขหรือดีบักในระหว่างการพัฒนาหรือในการผลิต

## <a name="access-logs-in-application-insights"></a>ล็อกอินการเข้าถึง Application Insights

หากต้องการเข้าถึงล็อกเหตุการณ์การวิเคราะห์ของส่วนประกอบ Commerce CSU และ Application Insights POS โดยผ่าน ให้ปฏิบัติตามขั้นตอนต่างๆ ในส่วนนี้ให้เสร็จสมบูรณ์

### <a name="minimum-version-requirements-for-csu"></a>ข้อกำหนดเวอร์ชันต่ำสุดสำหรับ CSU

CSU มีความต้องการเวอร์ชันต่ำสุดต่อไปนี้:

- 10.0.23 (เซิร์ฟเวอร์ Retail เวอร์ชัน 9.33.22062.15 และใหม่กว่า)
- 10.0.24 (เซิร์ฟเวอร์ Retail เวอร์ชัน 9.34.22062.14 และใหม่กว่า)
- 10.0.25 (เซิร์ฟเวอร์ Retail เวอร์ชัน 9.35.22062.13 และใหม่กว่า)
- 10.0.26 และใหม่กว่า (เวอร์ชันทั้งหมด)

### <a name="enable-diagnostic-events-in-application-insights"></a>เปิดใช้งานเหตุการณ์การวินิจฉัยใน Application Insights

> [!IMPORTANT]
> หากคุณใช้เวอร์ชันพรีวิวของ Operational Insights ก่อนหน้านี้ คุณต้องใช้กระบวนการต่อไปนี้เพื่อเปิดใช้งาน Operational Insights ด้วยวิธีนี้ ช่วยให้คุณมั่นใจได้ว่าการเข้าถึงเหตุการณ์ที่ไว้ใจได้และมีความปลอดภัยสามารถดำเนินการต่อได้

เมื่อต้องการเปิดใช้งานเหตุการณ์การวิเคราะห์ส่วนประกอบของ Commerce คุณต้องมีบัญชี Application Insights คุณสามารถใช้บัญชีที่มีอยู่ หรือ [สร้างบัญชีใหม่](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource) เนื่องจากเหตุผลด้านสิทธิส่วนบุคคลของข้อมูล เราขอแนะนำว่าคุณควรใช้บัญชี Application Insights แยกต่างหากสำหรับสภาพแวดล้อมการทำงาจริง sandbox และสภาพแวดล้อมการพัฒนา เมื่อคุณสร้างบัญชีแล้ว คุณต้องเปิดใช้งานคุณลักษณะ **Operational Insights** ในศูนย์ควบคุม

ในการเปิดใช้งานเหตุการณ์การวินิจฉัยใน Application Insights ให้ทำตามขั้นตอนเหล่านี้

1. ในศูนย์ควบคุม เปิดพื้นที่ทำงาน **การจัดการคุณลักษณะ** และเปิดใช้งานคุณลักษณะ **Operational Insights**
1. ไปที่ **การจัดการระบบ \> การตั้งค่า \> Operational Insights**
1. บนแท็บ **ตั้งค่าคอนฟิก** ให้ตั้งค่าตัวเลือก **เหตุการณ์ช่องทาง Commerce** เป็น **ใช่**
1. บนแท็บ **สภาพแวดล้อม** ให้ป้อน **รหัสสภาพแวดล้อม LCS** และ **โหมดสภาพแวดล้อม** ให้กับทุกสภาพแวดล้อมที่คุณวางแผนที่จะใช้ Application Insights คุณสามารถค้นหารหัสสภาพแวดล้อมของแต่ละสภาพแวดล้อมในหน้า **รายละเอียดสภาพแวดล้อม** ของสภาพแวดล้อมนั้นใน Microsoft Dynamics Lifecycle Services ขั้นตอนนี้ต้องใช้เพื่อป้องกันไม่ให้เหตุการณ์การวิเคราะห์ถูกส่งไปยังสภาพแวดล้อมที่ไม่ถูกต้องโดยไม่ได้ตั้งใจ เมื่อดําเนินการคัดลอกฐานข้อมูล
1. บนแท็บ **Application Insights รีจิสทรี** ให้ระบุค่า Application Insights **คีย์การรายงานข้อมูลระบบ** และค่าของ **โหมดสภาพแวดล้อม** ที่สอดคล้องกันของสภาพแวดล้อมที่คุณวางแผนที่จะใช้บัญชี Application Insights แต่ละรายการ
1. หลังจากที่คุณเสร็จสิ้นการตั้งค่าคอนฟิกก่อนหน้านี้แล้ว คุณต้องรันงาน **CDX Job 1110** คุณสามารถรอให้งานนี้รันในการจัดกำหนดการของตนเอง หรือคุณสามารถรันงานนี้ด้วยตนเองได้
1. ใน Lifecycle Services ให้ไปที่ **รายละเอียดสภาพแวดล้อม \> Commerce \> จัดการ** เลือกอินสแตนซ์ CSU แล้วเลือก **เริ่มใหม่** ทำขั้นตอนนี้ซ้ำสำหรับไซต์แต่ละ CSU
1. ทําซ้ําขั้นตอนก่อนหน้านี้ให้กับแต่ละสภาพแวดล้อมที่คุณวางแผนที่จะใช้ Application Insights

> [!NOTE]
> - เหตุการณ์การวัดและส่งข้อมูลทางไกล ใน Operational Insights อาจเปลี่ยนแปลงได้ ขอแนะนำให้คุณใช้เหตุการณ์ Operational Insights เพื่อทำการวิเคราะและการแก้ไขปัญหาเบื้องต้นด้วยตัวเอง ไม่ได้กําหนดแดชบอร์ดหรือข้อความแจ้งเตือน ถ้าคุณใช้เหตุการณ์เพื่อวัตถุประสงค์นอกเหนือจากการแก้ไขปัญหาเบื้องต้นแบบบริการตนเอง ขอแนะนาว่าคุณควรตรวจสอบความถูกต้องและอัปเดตการสอบถามของคุณหลังจากใช้งาน CSU/POS แต่ละครั้ง
> - ใน Commerce เวอร์ชัน 10.0.29 กระบวนการในส่วนนี้ยังเปิดใช้งานการสตรีมเหตุการณ์ POS Operational Insights กับบัญชี Application Insights ของคุณด้วย สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Operational Insights สำหรับ POS – เหตุการณ์และการสอบถาม](https://download.microsoft.com/download/9/2/b/92be35b0-0e24-4a4d-940d-6f4db29791c0/Operational-Insights-Commerce-POS-events-queries.pdf)

#### <a name="use-the-dllhostexeconfig-file-to-control-pos-operational-insights-events"></a>ใช้ไฟล์ DLLHost.exe.config เพื่อควบคุมเหตุการณ์ POS Operational Insights

ในการใช้ไฟล์ DLLHost.exe.config เพื่อควบคุมเหตุการณ์ POS Operational Insights ให้ทำตามขั้นตอนเหล่านี้

1. ในโปรแกรมแก้ไขข้อความ ให้เปิดไฟล์ **DLLHost.exe.config** ที่ **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker**
1. ในส่วน **diagnosticsSection** ให้ลบองค์ประกอบ XML ที่ซิงค์ซึ่งมีชื่อคลาส **Microsoft.Dynamics.Retail.Diagnostics.OperationalInsights.OperationalInsightsLogger**
1. บันทึกไฟล์

### <a name="disable-diagnostic-events-in-application-insights"></a>ปิดใช้งานเหตุการณ์การวินิจฉัยใน Application Insights

> [!IMPORTANT]
> หากคุณต้องการปิดใช้งานเหตุการณ์การวินิจฉัยและไม่ส่งไปยัง Application Insights อีกต่อไป คุณต้องปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ คุณไม่สามารถปิดใช้งานคุณลักษณะ ในการจัดการคุณลักษณะได้

ในการปิดใช้งานเหตุการณ์การวินิจฉัยใน Application Insights ให้ทำตามขั้นตอนเหล่านี้

1. ในศูนย์ควบคุม ให้ไปที่ **การจัดการระบบ \> Operational Insights**
1. บนแท็บ **ตั้งค่าคอนฟิก** ให้ตั้งค่าตัวเลือก **เหตุการณ์ช่องทาง Commerce** เป็น **ไม่**
1. หลังจากที่คุณเสร็จสิ้นการตั้งค่าคอนฟิกก่อนหน้านี้แล้ว คุณต้องรันงาน **CDX Job 1110** คุณสามารถรอให้งานนี้รันในการจัดกำหนดการของตนเอง หรือคุณสามารถรันงานนี้ด้วยตนเองได้
1. ใน Lifecycle Services ให้ไปที่ **รายละเอียดสภาพแวดล้อม \> Commerce \> จัดการ** เลือกอินสแตนซ์ CSU แล้วเลือก **เริ่มใหม่** ทำขั้นตอนนี้ซ้ำสำหรับไซต์แต่ละ CSU
1. ทําซ้ําขั้นตอนก่อนหน้านี้ให้กับแต่ละสภาพแวดล้อมที่คุณวางแผนที่จะปิด Application Insights

เมื่อต้องการปิดใช้งานเหตุการณ์การวิเคราะห์เฉพาะสภาพแวดล้อมเดียว ให้ลบคีย์เครื่องมือบนแท็บ **Application Insights รีจิสทรี** ของหน้า **Operational Insights** จากนั้นให้ปฏิบัติตามขั้นตอนที่ 3 และ 4 ของขั้นตอนก่อนหน้านี้

> [!NOTE]
> ใน Commerce เวอร์ชัน 10.0.29 และใหม่กว่า ขั้นตอนในส่วนนี้ยังปิดใช้งานการสตรีมเหตุการณ์ POS Operational Insights กับบัญชี Application Insights ของคุณด้วย 
