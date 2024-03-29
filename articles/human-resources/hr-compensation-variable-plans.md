---
title: สร้างแผนค่าตอบแทนผันแปร
description: บทความนี้อธิบายถึงส่วนประกอบที่ต้องตั้งค่าก่อนที่คุณจะสามารถใช้ค่าตอบแทนผันแปร และลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปร
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan, HcmCompensationWorkspace
audience: Application User
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: f2f51a095a23b651dca645b14e652519f20037e2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070572"
---
# <a name="create-variable-compensation-plans"></a>สร้างแผนค่าตอบแทนผันแปร


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

ค่าตอบแทนผันแปรทำให้ค่าตอบแทนของพนักงานไม่สม่ำเสมอ เช่นรางวัลหุ้นสามัญหรือโบนัส บทความนี้อธิบายวิธีการตั้งค่าส่วนประกอบที่จำเป็นสำหรับค่าตอบแทนผันแปร และลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปร

การคำนวณยอดเงินค่าตอบแทนผันแปรสำหรับพนักงานของคุณอาจขึ้นอยู่กับหลายปัจจัย เช่นประสิทธิภาพการทำงานของพนักงาน ระดับค่าตอบแทนของพนักงาน และประสิทธิภาพของแผนก

## <a name="variable-compensation-components"></a>ส่วนประกอบต่างๆของค่าตอบแทนผันแปร
### <a name="create-compensation-types"></a>สร้างชนิดค่าตอบแทนต่างๆ

**ชนิดค่าตอบแทนผันแปรชนิดต่างๆ** คือส่วนประกอบที่จำเป็น **ชนิดค่าตอบแทนผันแปร** อธิบายชนิดของค่าตอบแทนผันแปรซึ่งเป็นรางวัลขององค์กรคุณ พวกเขายังช่วยให้คุณสามารถระบุว่า ค่าตอบแทนจะเป็นเงินสด หรือ ในแบบ ฟอร์มที่ไม่เกี่ยวกับเงินตรา เช่น ปริมาณสินค้าคงคลัง

### <a name="describe-vesting-rules"></a>อธิบายกฎสิทธิ์พึงได้

อีกทางเลือกหนึ่งคือ บริษัทสามารถตั้งค่า **กฎสิทธิ์พึงได้** ได้ **กฎสิทธิ์พึงได้** อธิบายวิธีเงินรางวัลผันแปรควรปันส่วนตามช่วงเวลา ตัวอย่างเช่น กฎสิทธิ์พึงได้อาจระบุว่า พนักงานจะได้รับ 25 เปอร์เซ็นต์ของรางวัลรวมทุกปีอีกสี่ปีถัดไป กฎสิทธิ์พึงได้ต่างๆเป็นเพียงการให้ข้อมูลเท่านั้น

## <a name="variable-compensation-plans"></a>แผนค่าตอบแทนผันแปร
**แผนค่าตอบแทนผันแปร** ประกอบด้วยกฎ วิธีการคำนวณ และค่าเริ่มต้นสำหรับการคำนวณค่าตอบแทนผันแปรของพนักงานที่ลงทะเบียน เมื่อคุณสร้างแผนค่าตอบแทนผันแปร คุณต้องตั้งค่าชนิดค่าตอบแทนผันแปร ชนิดค่าตอบแทนผันแปรกำหนดว่า ระบบจะคำนวณเป็นยอดสกุลเงินหรือจำนวนหน่วยเป็นเงินรางวัล 

พารามิเตอร์ **จำกัดการเข้าถึงบทบาทที่เลือก** จํากัดการเข้าถึงแผนค่าตอบแทนให้กับ Security role ที่เลือก ซึ่งกําหนดให้กับแผนนั้นในทรัพยากรบุคคล ตัวอย่างเช่น เมื่อคุณสร้างแผนค่าตอบแทนที่ใช้เพื่อผู้บริหาร และไม่ควรสามารถเห็นได้โดยบทบาท HR ทั้งหมด คุณสามารถใช้พารามิเตอร์นี้เพื่อจํากัดการเข้าถึงแผนค่าตอบแทนดังกล่าวได้ 

ทั้งนี้คุณต้องกำหนดวิธีการคำนวณด้วย:

-   **ณ เวลานี้** – การคำนวณเงินรางวัลผันแปรจะขึ้นอยู่กับค่าตอบแทนคงที่พนักงานจะได้รับวันที่ที่ระบุไว้ มีระบุวันที่ในเหตุการณ์กระบวนการเมื่อยอดเงินค่าตอบแทนใหม่ถูกดำเนินการ
-   **โดยรวมแล้ว**– ยอดเงินรางวัลที่ได้คำนวณสำหรับอัตราค่าจ้างแต่ละค่าตอบแทนคงที่เฉพาะที่พนักงานมีระหว่างวันเริ่มต้นรอบและวันสิ้นสุดของวงจรในเหตุการณ์ในกระบวนการ อัตราต่างๆ จะถูกรวมเข้าด้วยกันเพื่อกำหนดเงินรางวัลขั้นสุดท้าย ตัวอย่างเช่น ในระหว่างวงจร พนักงานถูกโอนย้ายไปยังตำแหน่งอื่นที่มีอัตราค่าจ้างที่แตกต่างกัน ในกรณีนี้ เงินรางวัลผันแปรถูกปรับปรุงสำหรับระยะเวลาที่พนักงานได้อัตราค่าจ้างของแต่ละอัตรา

ยอดเงินของเงินรางวัลผันแปรสามารถขึ้นกับเปอร์เซ็นต์ของรายได้พื้นฐานปกติของพนักงานหรือจำนวนชุดของหน่วย

-   เลือก **เปอร์เซ็นต์ของตัวเลือกพื้นฐาน** เพื่อป้อนเปอร์เซ็นต์เริ่มต้น และระบุว่า ข้อมูลพื้นฐานของพนักงานควรเป็นอัตราค่าจ้างคงที่หรือจุดควบคุมตามระดับค่าตอบแทนของพนักงาน ระดับค่าตอบแทนถูกกำหนดไว้ในงานของพนักงาน จุดอ้างอิงจากโครงสร้างค่าตอบแทนหนึ่งสามารถตั้งค่าเป็นจุดควบคุมในแผนค่าตอบแทนคงที่ ระดับค่าตอบแทนจากงานของพนักงานจะใช้และอ้างอิงไขว้ไว้กับระดับของงานด้วยจุดควบคุมที่ระบุในแผนค่าตอบแทนคงที่ของพนักงานเพื่อหาจุดควบคุมของยอดเงินของระดับค่าตอบแทนพนักงาน โดยจุดควบคุมของยอดเงินนี้จะนำมาใช้แทนค่าจ้างคงที่ของพนักงานเพื่อเป็นข้อมูลพื้นฐานสำหรับรางวัล
-   เลือก **ตัวเลือกจำนวนหน่วย** เพื่อป้อนจำนวนเริ่มต้นของหน่วยต่างๆ มูลค่าของแต่ละหน่วยและสกุลเงินของมูลค่าต่อหน่วย ถ้าแผนค่าตอบแทนเป็นรางวัลที่ไม่ใช่เงินสด(ตัวอย่างเช่น 200 หน่วยของสินค้าคงคลังที่มีมูลค่า USD 40), หรือเป็นเพียงจำนวนของหน่วย ถ้าแผนค่าตอบแทนนั้นมีรางวัลเป็นเงินสด สำหรับรางวัลเงินสด พนักงานจะได้รับจำนวนหน่วยของสกุลเงินที่ใช้แผนค่าตอบแทนถาวร(ตัวอย่างเช่น 500 หน่วย ต่อ 1 USD) ตัวควบคุมความสัมพันธ์แบบหนึ่งต่อหนึ่งสามารถใช้เพื่อบ่งชี้ว่า มีการแมปหนึ่งต่อหนึ่งโดยตรงระหว่างจำนวนหน่วยและมูลค่าต่อหน่วย เมื่อคุณสร้างแผนค่าตอบแทนผันแปรสำหรับแผนแบบเงินสด โดยใช้จำนวนหน่วย ตัวเลือกนี้ถูกล็อคโดยอัตโนมัติไปยัง **ใช่** และมูลค่าต่อหน่วยคือ **1.0000**

**กฎการจ้างงาน** ระบุว่าพนักงานทั้งหมดควรได้รับการเพิ่มค่าตอบแทนเช่นเดียวกัน โดยไม่คำนึงถึงวันที่มีการจ้างงาน (**กฎการจ้างงาน** = **ไม่มี**) หรือว่าพนักงานควรได้รับรางวัลตามเปอร์เซ็นต์ ตามระยะเวลาที่พวกเขาได้ถูกว่าจ้างในระหว่างวงจร (**กฎการจ้างงาน** = **เปอร์เซ็นต์**) 

**ประสิทธิภาพการดำเนินงาน** ปรับปรุงรางวัลของพนักงาน ตามประสิทธิภาพของแผนกของพนักงาน สามารถกำหนดเครื่องมือวัดประสิทธิภาพสำหรับแต่ละแผนกได้ในหน้า **แผนก** ภายใต้ **รูปแบบที่สัมพันธ์กัน** &gt; **ค่าตอบแทน** &gt; **ประสิทธิภาพ** เงินรางวัลที่พนักงานในแผนกจะได้รับขึ้นอยู่กับค่าของฟิลด์ **เปอร์เซ็นต์ของเป้าหมายที่ทำได้** ซึ่งบ่งชี้ถึงประสิทธิภาพการทำงานของแผนก:

-   ถ้า ประสิทธิภาพของแผนกคือ100 เปอร์เซ็นต์ รางวัลสำหรับพนักงานในแผนกที่จะพิจารณาตามเปอร์เซ็นต์ที่กำหนดไว้ใน **การจ่ายเงินจะอยู่ที่ฟิลด์ 100%**
-   ถ้า ประสิทธิภาพของแผนกมากกว่า 100 เปอร์เซ็นต์ ระบบจะเพิ่มเปอร์เซ็นต์ที่กำหนดไว้ในฟิลด์ **เกินเป้าหมาย 1%** กับเปอร์เซ็นต์ที่กำหนดไว้ในฟิลด์ **การชำระที่ 100%** จนถึงค่าที่กำหนดไว้ในฟิลด์ **ชำระสูงสุดที่ยอมรับ** ได้
-   ถ้า ประสิทธิภาพของแผนกน้อยกว่า 100 เปอร์เซ็นต์ ระบบจะหักเปอร์เซ็นต์ที่กำหนดไว้ในฟิลด์ **ต่ำกว่าเป้าหมาย 1%** จากเปอร์เซ็นต์ที่กำหนดไว้ในฟิลด์ **การชำระใน 100%** จนถึงค่าที่กำหนดไว้ในฟิลด์ **ชำระต่ำที่สุดที่ยอมรับ** ได้

**ระดับค่าเผื่อ** สามารถตั้งค่าตามเปอร์เซ็นต์ขีดจำกัด, เพื่อให้ข้อความแจ้งเตือนปรากฏขึ้นถ้าค่าใช้จ่ายจะเป็นสาเหตุให้เปอร์เซนต์นั้นอยู่นอกเปอร์เซ็นต์ขีดจำกัด 

โดยค่าเริ่มต้น แผนกที่จะกำหนดตำแหน่งของพนักงานจะใช้สำหรับเงินรางวัลของพนักงาน อย่างไรก็ตาม รางวัลสำหรับพนักงานบางคนอาจขึ้นอยู่กับประสิทธิภาพของแผนกต่างๆ ในกรณีนี้ แผนกต่าง ๆ และเปอร์เซ็นต์ของรางวัลที่ปันส่วนให้ประสิทธิภาพการทำงานของแต่ละแผนกสามารถกำหนดใน "การลงทะเบียนค่าตอบแทนผันแปรของพนักงาน" สำหรับข้อมูลเพิ่มเติม โปรดดูที่ส่วน "การลงทะเบียนสำหรับค่าตอบแทนผันแปร" ดังต่อไปนี้ 

ระดับการใช้ค่าใช้จ่ายใช้เฉพาะถ้า **ค่าจ้างสำหรับประสิทธิภาพการทำงาน** ถูกเลือกเมื่อได้ดำเนินกระบวนการค่าตอบแทน 

แท็บ **ระดับการแทนที่** ช่วยให้คุณสามารถแทนเปอร์เซ็นต์เริ่มต้นของเงินรางวัลหรือจำนวนหน่วย ตามระดับค่าตอบแทนของพนักงาน ถ้า **การแทนเปิดใช้งานสำหรับระดับ** ถูกตั้งค่าเป็น **ใช่** สำหรับพนักงานผู้เข้าร่วมในแผนค่าตอบแทนผันแปร ระดับจากงานของพนักงานจะเปรียบเทียบกับระดับตารางแทนที่เพื่อกำหนดเปอร์เซ็นต์หรือจำนวนหน่วยสำหรับระดับนั้น ถ้าไม่พบระดับในตารางระดับการแทนที่ เปอร์เซ็นต์เริ่มต้น หรือจำนวนของหน่วยจากแท็บ **ทั่วไป** จะถูกใช้ เปอร์เซ็นต์และจำนวนหน่วยยังสามารถแทนที่ในการลงทะเบียนของพนักงานในแผนค่าตอบแทนผันแปร

## <a name="variable-compensation-enrollment"></a>การลงทะเบียนสำหรับค่าตอบแทนผันแปร
### <a name="determine-who-is-eligible-for-the-plan"></a>ตรวจสอบผู้ที่มีคุณสมบัติเหมาะสมกับแผน

เมื่อคุณพร้อมที่จะลงทะเบียนพนักงานในแผนค่าตอบแทนแปรผัน ขั้นแรกจะกำหนดว่าใครมีมีสิทธิ์ที่จะได้รับค่าตอบแทนที่ระบุไว้ในแผน คุณไม่สามารถกำหนดแบบแผนให้กับพนักงานใดๆ จนกว่าคุณกำหนดสิทธิ์ที่จะได้รับเลือก เมื่อต้องการตั้งค่าสิทธิ์ เปิดหน้า **กฎการมีสิทธิ์** เพื่อสร้างสิทธิ์การสร้างกฎสำหรับแผนค่าตอบแทนของคุณ แล้วกำหนดเงื่อนไขซึ่งพนักงานต้องตรงตามคุณสมบัติเพื่อให้มีสิทธิ์สำหรับแผนค่าตอบแทน คุณสามารถจำกัดสิทธิ์โดยแผนก สหภาพแรงงาน ค่าตอบแทนตามภูมิภาค (ที่ตั้ง), งาน หน้าที่งาน ชนิดงาน และ/หรือระดับค่าตอบแทน พนักงานสามารถลงทะเบียนในแผนค่าตอบแทนเฉพาะเมื่อพวกเขาปฏิบัติตามเงื่อนไข **ทั้งหมด** ที่กำหนดไว้ในฎการมีสิทธิ์ 

**หมายเหตุ:** การกำหนดคุณสมบัติกฎการมีสิทธิ์สำหรับทั้งแผนค่าตอบแทนคงที่ และแผนค่าตอบแทนผันแปร กฎการมีสิทธิ์พิจารณาค่าของฟิลด์ที่ระบุในงาน ตำแหน่ง และบันทึกข้อมูลพนักงานเพื่อกำหนดพนักงานว่ามีสิทธิสำหรับแผนค่าตอบแทน

- ในหน้า **งาน** :
  -   ฟิลด์ **งาน** นั้น
  -   ในฟิลด์ **ฟังก์ชั่น** และ **ชนิดงาน** ในแท็บ **การจัดประเภทงาน** นั้น
  -   ในฟิลด์ **ระดับ** ในแท็บ **ค่าตอบแทน** นั้น
- ในหน้า **ตำแหน่ง** : ฟิลด์ **แผนก** และ **ฟิลด์ภูมิภาคของค่าตอบแทน** นั้น
- ในหน้า <strong>พนักงาน</strong> : ข้อมูลเกี่ยวกับสหภาพแรงงานที่เชื่อมโยงกับพนักงานภายใต้ <strong>ข้อมูลส่วนบุคคล</strong> &gt; <strong>สหภาพแรงงาน</strong> ในแท็บ *<strong><em>ผู้ปฏิบัติการ</em></strong>* นั้น

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>เปิดใช้งานการลงทะเบียนสำหรับแผนค่าตอบแทนผันแปร

ใน **หน้าแผนค่าตอบแทนผันแปร**, ตั้ง **ตัวเลือกเปิดใช้งานการลงทะเบียน** ไปยัง **ใช่** เพื่ออนุญาตให้พนักงานลงทะเบียนในแผนสิทธิ์

### <a name="enroll-the-employee"></a>การลงทะเบียนพนักงาน

คุณสามารถลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปรได้ตอนนี้ เมื่อต้องการลงทะเบียนพนักงาน ไปที่ **หน้าพนักงาน** และเลือกพนักงาน จากนั้น บนบานหน้าต่างการดำเนินการ คลิก **การลงทะเบียน** &gt; **แผนค่าตอบแทนผันแปร** 

**หมายเหตุ:** **การลงทะเบียน** ต้องถูกกำหนดเป็น **ใช่** บนแผนค่าตอบแทนผันแปร ฟิลด์ **แผน** แสดงแผนที่พนักงานมีคุณสมบัติเหมาะสม ตามกฎการมีสิทธิ์ที่จะตั้งค่าสำหรับแผนเหล่านั้น ถ้ากฎการมีสิทธิ์ไม่ได้ตั้งค่าสำหรับแผนใดแผนหนึ่ง ก็จะไม่มีพนักงานที่จะมีสิทธิ์สำหรับแผนนั้น 

ตรวจสอบให้แน่ใจว่าฟิลด์ **วันมีผลบังคับใช้** ถูกตั้งค่าอย่างถูกต้อง ถ้าแผนค่าตอบแทนผันแปรใช้วิธีการคำนวณ **โดยรวม** วันที่มีผลบังคับใช้ของการลงทะเบียนอาจพิจารณาในระหว่างการคำนวณรางวัลของพนักงานได้ 

คุณสามารถใช้แท็บ **แท็บการแทนที่** เพื่อแทนค่าที่เฉพาะเจาะจงสำหรับพนักงานได้ ตัวอย่างเช่น ถ้า **กฎการจ้างงาน** ถูกตั้งค่าเป็น **เปอร์เซ็นต์** ในแผน และในฟิลด์วันจ้างงานควรใช้ระหว่างการคำนวณเปอร์เซ็นต์การจ้างงานของพนักงาน คุณสามารถตั้งค่าวันจ้างงานในฟิลด์ **วันที่ของกฎการจ้างงาน** คุณสามารถแทนที่ด้วยค่า **เปอร์เซ็นต์เงินรางวัล** หรือค่า **จำนวนหน่วย** สำหรับพนักงานแต่ละคน ซึ่งขึ้นอยู่กับการตั้งค่าของแผนได้ ค่าเหล่านี้จะยังคงถูกพิจารณา โดยกฎการจ้างงาน ปัจจัยด้านประสิทธิภาพ และการตั้งค่าอื่นๆ ในแผน 

**การแทนที่ในระดับองค์กร** ใช้ในการให้รางวัลของพนักงานยึดตามประสิทธิภาพของแผนกหนึ่งรายการขึ้นไป เปอร์เซ็นต์ที่จะปันส่วนแผนกควรเป็น 100 เปอร์เซ็นต์ นอกจากนี้ยังมีการพิจารณาประสิทธิภาพการทำงานของพนักงานรายบุุคล การตั้งค่าเหล่านี้จะถูกใช้เฉพาะถ้า **ค่าจ้างสำหรับประสิทธิภาพ** ถูกกำหนดไว้เมื่อมีการดำเนินกระบวนการค่าตอบแทน





[!INCLUDE[footer-include](../includes/footer-banner.md)]
