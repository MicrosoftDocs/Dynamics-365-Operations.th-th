---
title: การเติมสินค้าสินค้าคงคลังที่ปลอดภัยสำหรับสินค้า
description: บทความนี้อธิบายการเติมสินค้าสินค้าคงคลังที่ปลอดภัยและวิธีการตั้งค่าปริมาณสินค้าคงคลังที่ปลอดภัยสำหรับสินค้า
author: t-benebo
ms.date: 8/23/2021
ms.topic: article
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 70461ad1de94c984cb41e6b1d46af9e310a928d6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887412"
---
# <a name="safety-stock-fulfillment-for-items"></a>การเติมสินค้าสินค้าคงคลังที่ปลอดภัยสำหรับสินค้า

[!include [banner](../includes/banner.md)]

สินค้าคงคลังที่ปลอดภัยบ่งชี้ปริมาณของสินค้าเพิ่มเติมที่จัดเก็บไว้ในสินค้าคงคลัง เพื่อลดความเสี่ยงที่จะไม่มีสินค้าในสินค้าคงคลัง คุณสามารถใช้สินค้าคงคลังที่ปลอดภัยเป็นสินค้าคงคลังบัฟเฟอร์ในกรณีที่ใบสั่งขายเข้ามา และซัพพลายเออร์ไม่สามารถจัดส่งสินค้าเพิ่มเติมเพื่อให้ตรงกับวันที่จัดส่งที่ร้องขอของลูกค้าได้ เมื่อสินค้าคงคลังที่ปลอดภัยถูกใช้ในการตอบสนองใบสั่งขาย สินค้าคงคลังที่ปลอดภัยจะถูกลด คุณสามารถใช้การวางแผนหลักเพื่อทำให้สินค้าคงคลังกลับไปที่ระดับความปลอดภัยโดยอัตโนมัติ

## <a name="set-up-safety-stock-levels-for-items"></a>ตั้งค่าระดับปริมาณสินค้าคงคลังที่ปลอดภัยสำหรับสินค้า

สินค้าคงคลังที่ปลอดภัยถูกตั้งค่าให้เป็นส่วนหนึ่งของความครอบคลุมสินค้าบนหน้า **ความครอบคลุมสินค้า** ภายใต้ **ผลิตภัณฑ์ที่นำออกใช้ \> แผน \> ความครอบคลุม**

ในฟิลด์ **ต่ำสุด** ป้อนระดับสินค้าคงคลังที่ปลอดภัยที่คุณต้องการรักษาสำหรับสินค้า ค่าจะแสดงในหน่วยสินค้าคงคลัง  ถ้าคุณปล่อยฟิลด์ว่างไว้ ค่าเริ่มต้นจะเป็นศูนย์ ฟิลด์นี้จะพร้อมใช้งานเมื่อคุณเลือก **รอยระยะเวลา** **ความต้องการ** หรือ **ค่าน้อยสุด/ค่ามากสุด** ในรายการ **รหัสความครอบคลุม** ขีดจำกัดระดับปริมาณสินค้าคงคลังใช้กับสินค้าคงคลังที่พร้อมใช้งาน ซึ่งหมายความว่าการจองและการทำเครื่องหมายอาจทริกเกอร์การเติมสินค้าคงคลังที่ปลอดภัย ก่อนที่ปริมาณทางกายภาพจะต่ำกว่าระดับต่ำสุดที่ระบุ

> [!NOTE]
> คุณต้องกำหนดมิติความครอบคลุมที่วางแผนไว้อื่นๆ ทั้งหมด ก่อนที่คุณจะสามารถกำหนดฟิลด์ **ต่ำสุด** ได้ ซึ่งป้องกันเรกคอร์ดที่ไม่ถูกต้องไม่ให้มีการใช้ในระหว่างการวางแผนหลัก สถานการณ์นี้อาจเกิดขึ้นได้ ตัวอย่างเช่น ถ้ากลุ่มมิติถูกขยายด้วยมิติความครอบคลุมที่วางแผนไว้เพิ่มเติม สำหรับที่ปริมาณสินค้าคงคลังต่ำสุดและสูงสุดยังไม่ได้ถูกกำหนด

คุณสามารถใช้คีย์ต่ำสุดในการจัดการความผันผวนของความต้องการสินค้าเนื่องจากฤดูกาลได้ ตัวอย่างเช่น คุณสามารถลดระดับสินค้าคงคลังต่ำสุดสำหรับสินค้าในช่วงนอกฤดูกาลได้ และจากนั้นเพิ่มระดับขึ้นทีละน้อยในเดือนต่อๆ ไป คุณสร้างคีย์ต่ำสุดโดยการไปยัง **การวางแผนหลัก \> การตั้งค่า \> ความครอบคลุม \> คีย์ต่ำสุด/สูงสุด** คุณระบุคีย์ต่ำสุดเพื่อปรับปรุงระดับสินค้าคงคลังที่ปลอดภัยตามช่วงเวลาในฟิลด์ **คีย์ต่ำสุด** ในหน้า **ความครอบคลุมสินค้า**

## <a name="example-minimum-key"></a>ตัวอย่าง: คีย์ต่ำสุด

กระบวนงานต่อไปนี้เป็นตัวอย่างที่แสดงวิธีการตั้งค่าคีย์ต่ำสุดที่อธิบายความต้องการที่เพิ่มขึ้นตามฤดูกาลระหว่างช่วงเดือนฤดูใบไม้ผลิถึงฤดูร้อน

1. ไปยัง **การวางแผนหลัก \> การตั้งค่า \> ความครอบคลุม \> คีย์ต่ำสุด/สูงสุด**
1. เลือก **สร้าง** เพื่อสร้างคีย์ต่ำสุด/สูงสุด
1. ในฟิลด์ **คีย์ต่ำสุดหรือสูงสุด** ป้อนตัวระบุสำหรับคีย์ ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับคีย์
1. ตั้งค่าตัวเลือก **ใช้วันที่มีผลบังคับใช้** เป็น *ใช่* และปล่อยฟิลด์ **วันที่มีผลบังคับใช้** ให้ว่างไว้ เพื่อทำให้คีย์มีผลบังคับใช้ตั้งแต่วันแรกของปีปัจจุบัน

    > [!NOTE]
    > ชุดของการตั้งค่า **ใช้วันที่มีผลบังคับใช้** และ **วันที่มีผลบังคับใช้** จะกําหนดวันที่เริ่มต้นการมีผลบังคับใช้ของคีย์
    >
    > - เมื่อมีการตั้งค่าตัวเลือก **ใช้วันที่มีผลบังคับใช้** เป็น *ไม่* คีย์จะมีผลบังคับใช้ตั้งแต่วันที่ปัจจุบันหรือวันที่ของระบบ
    > - เมื่อมีการตั้งค่าตัวเลือก **ใช้วันที่มีผลบังคับใช้** เป็น *ใช่* และคีย์มีผลบังคับใช้ตั้งแต่วันที่ที่ถูกกําหนดไว้ในฟิลด์ **วันที่มีผลบังคับใช้**

1. ในส่วน **รอบระยะเวลา** ให้สร้างบรรทัด 12 บรรทัด และตั้งค่าต่อไปนี้ให้บรรทัดเหล่านั้น:

    - **เปลี่ยน** – กําหนดหมายเลขเฉพาะให้แต่ละบรรทัดตั้งแต่ 1 ถึง 12 ฟิลด์นี้จะระบุการเปลี่ยนแปลงส่วนเพิ่มในหน่วยเวลาที่ถูกกำหนดโดยฟิลด์ **หน่วย**
    - **หน่วย** – เลือก *เดือน* สำหรับทุกบรรทัด
    - **วันที่เริ่มต้น**, **วันที่สิ้นสุด**, และ **เดือน** – ฟิลด์เหล่านี้ถูกตั้งค่าโดยอัตโนมัติตามการตั้งค่า **เปลี่ยนแปลง** และ **หน่วย** รอบระยะเวลารายเดือนจะเริ่มต้นจากวันแรกของปีปัจจุบัน
    - **ตัวคูณ** – ป้อนค่าที่อธิบายไว้ในตารางต่อไปนี้ ฟิลด์นี้จะกําหนดตัวคูณที่คุณต้องการใช้คูณสินค้าคงคลังต่ำสุด

        | บรรทัด (เปลี่ยนแปลง) | แฟคเตอร์การทำงาน | ผลลัพธ์ |
        |---|---|---|
        | 1–3 | 1 | สินค้าคงคลังต่ำสุดจะขึ้นอยู่กับการตั้งค่าสำหรับเดือนมกราคมถึงมีนาคมในหน้า **ความครอบคลุมสินค้า** |
        | 4–5 | 2 | สินค้าคงคลังต่ำสุดจะคูณ 2 ในช่วงเดือนเมษายนถึงพฤษภาคม |
        | 6–8 | 2.5 | สินค้าคงคลังต่ำสุดจะคูณ 2.5 ในช่วงเดือนมิถุนายนถึงสิงหาคม |
        | 9–12 | 1 | สินค้าคงคลังต่ำสุดจะเปลี่ยนเป็นการตั้งค่าสำหรับเดือนกันยายนถึงธันวาคมในหน้า **ความครอบคลุมสินค้า** |

    ขณะนี้การตั้งค่าของคุณควรจะคล้ายกับการตั้งค่าในภาพประกอบต่อไปนี้

    ![รอบระยะเวลาของคีย์ต่ำสุดหรือสูงสุด](media/min-max-key-periods.png "รอบระยะเวลาของคีย์ต่ำสุดหรือสูงสุด")

> [!NOTE]
> นอกจากนี้ คุณยังสามารถใช้วิซาร์ดเพื่อสร้างคีย์ต่ำสุด/สูงสุด บนหน้า **คีย์ต่ำสุดหรือสูงสุด** ในบานหน้าต่างการดำเนินการ ให้เลือก **วิซาร์ด** เพื่อเปิดวิซาร์ด **คีย์ต่ำสุด/สูงสุด** วิซาร์ดจะแนะนำคุณทีละขั้นตอนเกี่ยวกับกระบวนการในการสร้างและการตั้งค่าคีย์ต่ำสุด/สูงสุด

ถ้ารหัสความครอบคลุมเป็น *ต่ำสุด/สูงสุด* คุณยังสามารถระบุปริมาณสินค้าคงคลังสูงสุดที่คุณต้องการรักษาสำหรับสินค้าได้ ค่ายังจะแสดงในหน่วยสินค้าคงคลังอีกด้วย ถ้าสินค้าคงคลังที่พร้อมใช้งานที่คาดการณ์ลดต่ำกว่าปริมาณต่ำสุด การวางแผนหลักจะสร้างแผนการใบสั่ง เพื่อเติมเต็มความต้องการที่เปิดทั้งหมด และทำให้ปริมาณสินค้าคงคลังที่พร้อมใช้งานเพิ่มขึ้นถึงปริมาณสูงสุดที่ระบุ เช่นเดียวกับเวลาที่คุณตั้งค่าปริมาณสินค้าคงคลังต่ำสุด คุณต้องกำหนดมิติความครอบคลุมที่วางแผนไว้อื่นๆ ทั้งหมด ก่อนที่คุณจะสามารถกำหนดฟิลด์ **ต่ำสุด** ได้

## <a name="example-minmax-coverage-code"></a>ตัวอย่าง: รหัสความครอบคลุมต่ำสุด/สูงสุด

ปริมาณต่ำสุดคือ 10 และปริมาณสูงสุดคือ 15 ปริมาณคงคลังคงเหลือปัจจุบันคือ 4 ส่งผลให้มีความต้องการสินค้าปริมาณต่ำสุดจำนวน 6 อย่างไรก็ตาม ปริมาณคงคลังคงเหลือปัจจุบันคือ 4 ซึ่งให้ความต้องการปริมาณขั้นต่ำเป็น 6 อย่างไรก็ตาม เนื่องจากปริมาณสูงสุดคือ 15 การวางแผนหลักสร้างใบสั่งที่วางแผนไว้สำหรับสินค้า 11 รายการ

สำหรับสินค้าที่เป็นไปตามความต้องการตามฤดูกาล คุณอาจต้องรักษาระดับสูงสุดที่แตกต่างกัน เมื่อต้องการทำเช่นนั้น คุณต้องกำหนด **คีย์สูงสุด** โดยการไปยัง **การวางแผนหลัก \> การตั้งค่า \> ความครอบคลุม \> คีย์ต่ำสุด/สูงสุด** กรอกข้อมูลฟิลด์ **คีย์สูงสุด** ในหน้า **ความครอบคลุมสินค้า** คุณสามารถดูข้อมูลเกี่ยวกับระดับปริมาณสินค้าคงคลังที่ปลอดภัยได้ ซึ่งกำหนดผ่านคีย์ต่ำสุดบนแท็บ **ต่ำสุด/สูงสุด** บนหน้า **ความครอบคลุมสินค้า** คุณต้องตรวจสอบให้แน่ใจว่า สำหรับระยะเวลาหนึ่ง ค่าต่ำสุดและค่าสูงสุดจะถูกซิงค์

## <a name="safety-stock-fulfillment"></a>การเติมสินค้าสินค้าคงคลังที่ปลอดภัย

พารามิเตอร์ **เติมสินค้าตามเกณฑ์ขั้นต่ำ** อนุญาตให้คุณสามารถเลือกวันที่ หรือรอบระยะเวลาระหว่างที่ระดับสินค้าคงคลังต้องตรงกับปริมาณที่คุณระบุไว้ในฟิลด์ **ค่าต่ำสุด** ฟิลด์นี้จะพร้อมใช้งานเมื่อคุณเลือก **รอยระยะเวลา** **ความต้องการ** หรือ **ค่าน้อยสุด/ค่ามากสุด** ในรายการ **รหัสความครอบคลุม**

ถ้ามีการใช้ **คีย์ต่ำสุด** เลือกกล่องกาเครื่องหมาย **รอบระยะเวลาต่ำสุด** เพื่อเติมระดับสินค้าคงคลังขั้นต่ำ สำหรับรอบระยะเวลาทั้งหมดที่ตั้งค่าไว้ในคีย์ต่ำสุด ถ้าคุณยกเลิกการเลือกกล่องกาเครื่องหมายนี้ จะมีการเติมสินค้าคงคลังขั้นต่ำสำหรับรอบระยะเวลาปัจจุบันเท่านั้น

สถานการณ์จำลองต่อไปนี้แสดงลักษณะการทำงานของพารามิเตอร์นี้ และความแตกต่างระหว่างค่า

> [!NOTE]
> สำหรับภาพประกอบในบทความนี้ทั้งหมด แกน x แสดงถึงสินค้าคงคลัง แกน y แสดงถึงจำนวนวัน แถบแสดงระดับสินค้าคงคลัง ลูกศรแสดงถึงธุรกรรม เช่น รายการใบสั่งขาย รายการใบสั่งซื้อ หรือใบสั่งที่วางแผนไว้

[![สถานการณ์ทั่วไปสำหรับการเติมสินค้าสินค้าคงคลังที่ปลอดภัย](media/Scenario1.png)](media/Scenario1.png)

พารามิเตอร์ **เติมสินค้าตามเกณฑ์ขั้นต่ำ** สามารถมีค่าดังต่อไปนี้:

### <a name="todays-date"></a>วันที่ของวันนี้

ปริมาณต่ำสุดที่ระบุตรงกับในวันที่ที่มีการรันการวางแผนหลัก ระบบพยายามจะเติมสินค้าตามขีดจำกัดสินค้าคงคลังที่ปลอดภัยโดยเร็วที่สุด ถึงแม้ว่าอาจจะเป็นไปไม่ได้ เนื่องจากเวลารอคอยสินค้า

[![ความต้องการในวันที่ของวันนี้](media/TodayReq.png)](media/TodayReq.png)

ใบสั่งที่วางแผนไว้ P1 ถูกสร้างขึ้นสำหรับวันที่ของวันนี้ เพื่อทำให้สินค้าคงคลังที่พร้อมใช้งานสูงกว่าระดับสินค้าคงคลังที่ปลอดภัยในวันที่นี้ รายการใบสั่งขายที่ S1 ถึง S3 ลดระดับสินค้าคงคลังต่อไป ใบสั่งที่วางแผนไว้ P2 ถึง P4 ถูกสร้างขึ้นโดยการวางแผนหลัก เพื่อให้ระดับสินค้าคงคลังถูกเลื่อนกลับมายังขีดจำกัดความปลอดภัย หลังจากความต้องการของใบสั่งขายแต่ละรายการ

เมื่อมีการใช้รหัสความครอบคลุม **ความต้องการ** จะมีการสร้างใบสั่งที่วางแผนไว้แบบหลายใบ มักแนะนำให้ใช้ความครอบคลุม **รอบระยะเวลา** หรือ **ต่ำสุด/สูงสุด** อย่างใดอย่างหนึ่ง สำหรับสินค้าและวัสดุที่ต้องการบ่อย เพื่อรวมการเติมสินค้า ในภาพต่อไปนี้แสดงตัวอย่างสำหรับรหัสความครอบคลุม **รอบระยะเวลา**

[![รอบระยะเวลา วันที่ของวันนี้](media/TodayPeriod.png)](media/TodayPeriod.png)

ภาพประกอบต่อไปนี้แสดงตัวอย่างสำหรับรหัสความครอบคลุม **ต่ำสุด/สูงสุด**

[![ต่ำสุด/สูงสุด วันที่ของวันนี้](media/TodayMinMax.png)](media/TodayMinMax.png)

### <a name="todays-date--procurement-time"></a>วันที่ของวันนี้ + เวลาการจัดหา

ปริมาณต่ำสุดที่ระบุตรงกับในวันที่ที่รันการวางแผนหลัก บวกกับระยะเวลารอคอยสินค้าที่สั่งซื้อหรือระยะเวลารอสินค้าจากการผลิต เวลานี้รวมถึงค่าเผื่อความปลอดภัยใดๆ ถ้าสินค้ามีข้อตกลงทางการค้า และมีการเลือกกล่องกาเครื่องหมาย **ค้นหาข้อตกลงทางการค้า** ในหน้า **พารามิเตอร์การวางแผนหลัก** ระยะเวลารอคอยสินค้าจากการจัดส่งจากข้อตกลงทางการค้าจะไม่มีการนำมาพิจารณา ระบบจะใช้ระยะเวลารอคอยสินค้าจากการตั้งค่าความครอบคลุมของสินค้าหรือจากสินค้า

โหมดการเติมสินค้านี้จะสร้างแผนที่มีความล่าช้าที่น้อยลงและใบสั่งที่วางแผนไว้ไม่กี่รายการ โดยไม่คำนึงถึงการตั้งค่ากลุ่มความครอบคลุมในสินค้า

ภาพประกอบต่อไปนี้แสดงผลลัพธ์ของแผน ถ้ารหัสความครอบคลุมคือ **ความต้องการ** หรือ **รอบระยะเวลา**

[![ความต้องการหรือระยะเวลา วันที่ของวันนี้ และระยะเวลารอคอยสินค้า](media/TodayPLTReq.png)](media/TodayPLTReq.png)

ภาพประกอบต่อไปนี้แสดงผลลัพธ์ของแผน ถ้ารหัสความครอบคลุมคือ **ต่ำสุด/สูงสุด**

[![ต่ำสุด/สูงสุด วันที่ของวันนี้ และระยะเวลารอคอยสินค้า](media/TodayPLTMinMax.png)](media/TodayPLTMinMax.png)

### <a name="first-issue"></a>การตัดสินค้าจากคลังครั้งแรก

ปริมาณต่ำสุดที่ระบุเป็นไปตามวันที่ที่สินค้าคงคลังที่พร้อมใช้งานลดต่ำกว่าระดับต่ำสุด ดังที่แสดงในภาพประกอบต่อไปนี้ แม้ว่าสินค้าคงคลังที่มีอยู่จะต่ำกว่าระดับต่ำสุดในวันที่ที่การวางแผนหลักทำงาน **การตัดสินค้าจากคลังครั้งแรก** จะไม่พยายามครอบคลุม จนกว่าจะมีความต้องการต่อไป

ในภาพต่อไปนี้แสดงตัวอย่างสำหรับรหัสความครอบคลุม **ความต้องการ**

[![การวางแผนสินค้าด้วยรหัสความครอบคลุมความต้องการ และการเติมสินค้าการตัดสินค้าจากคลังครั้งแรก](media/FirstIssueReq.png)](media/FirstIssueReq.png)

ในภาพต่อไปนี้แสดงตัวอย่างสำหรับรหัสความครอบคลุม **รอบระยะเวลา**

[![การวางแผนสินค้าด้วยรหัสความครอบคลุมรอบระยะเวลา และการเติมสินค้าการตัดสินค้าจากคลังครั้งแรก](media/FirstIssuePeriod.png)](media/FirstIssuePeriod.png)

ภาพประกอบต่อไปนี้แสดงตัวอย่างสำหรับรหัสความครอบคลุม **ต่ำสุด/สูงสุด**

[![การวางแผนสินค้าด้วยรหัสความครอบคลุม MinMax และการเติมสินค้าการตัดสินค้าจากคลังครั้งแรก](media/FirstIssueMinMax.png)](media/FirstIssueMinMax.png)

ในวันที่ที่การวางแผนหลักทำงาน ถ้าสินค้าคงคลังที่พร้อมใช้งานมีอยู่แล้วภายใต้ขีดจำกัดสินค้าคงคลังที่ปลอดภัย **วันที่ของวันนี้** และ **วันที่ของวันนี้ + เวลาในการจัดหา** จะทริกเกอร์การเติมสินค้าในทันที **การตัดสินค้าจากคลังครั้งแรก** จะรอจนกว่าจะไม่มีธุรกรรมการตัดสินค้าอื่น เช่น ใบสั่งขายและข้อกำหนดรายการ BOM สำหรับสินค้า และจากนั้น จึงจะทริกเกอร์การเติมสินค้าในวันที่ของธุรกรรมนี้

ในวันที่ที่การวางแผนหลักทำงาน ถ้าสินค้าคงคลังที่พร้อมใช้งานไม่ได้อยู่ภายใต้ขีดจำกัดสินค้าคงคลังที่ปลอดภัย **วันที่ของวันนี้** และ **การตัดสินค้าจากคลังครั้งแรก** จะแสดงผลลัพธ์เดียวกันทุกประการ ดังที่แสดงในภาพประกอบต่อไปนี้

[![ไม่อยู่ภายใต้ขีดจำกัด](media/ReqFirstIssue.png)](media/ReqFirstIssue.png)

ในวันที่ที่การวางแผนหลักทำงาน ถ้าสินค้าคงคลังที่พร้อมใช้งานไม่ได้อยู่ภายใต้ขีดจำกัดสินค้าคงคลังที่ปลอดภัย **วันที่ของวันนี้ + เวลาในการจัดหา** จะแสดงผลลัพธ์ดังต่อไปนี้ เนื่องจากจะเลื่อนการเติมสินค้าจนถึงจุดสิ้นสุดของระยะเวลารอคอยการจัดซื้อ

![การเติมสินค้าเลื่อนออกไปจนกว่าจะสิ้นสุดระยะเวลารอคอยสินค้าของการจัดซื้อ](media/ReqTodayLT.png)

### <a name="coverage-time-fence"></a>กรอบเวลาความครอบคลุม

ปริมาณต่ำสุดที่ระบุตรงกับในระหว่างรอบระยะเวลาที่ระบุในฟิลด์ **กรอบเวลาความครอบคลุม** ตัวเลือกนี้มีประโยชน์ เมื่อการวางแผนหลักไม่อนุญาตให้สินค้าคงคลังที่พร้อมใช้งานให้ถูกใช้สำหรับใบสั่งจริง เช่น การขายหรือการโอนย้าย ในความพยายามในการรักษาระดับความปลอดภัย อย่างไรก็ตาม ในรุ่นต่อไป โหมดของการเติมสินค้านี้จะไม่จำเป็นอีกต่อไป และตัวเลือกนี้จะถูกยกเลิกการใช้

## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>วางแผนการเติมสินค้าคงคลังด้านความปลอดภัยสำหรับสินค้าที่หมดอายุก่อน ออกก่อน (FEFO)

เมื่อใดก็ได้ในเวลา จะใช้สำหรับสต็อกปลอดภัยใบรับสินค้าคงคลัง ด้วยวันหมดอายุล่าสุดเพื่ออนุญาตจริงอุปสงค์ เช่นการขายหรือบรรทัด BOM เป็นเกณฑ์ผ่านในลำดับ FEFO (หมดอายุแรก แรกออก)

เมื่อต้องการแสดงวิธีใช้ พิจารณาสถานการณ์จำลองต่อไปนี้

[![สถานการณ์จำลอง FEFO](media/FEFOScenario.png)](media/FEFOScenario.png)

เมื่อมีการรันการวางแผน จะครอบคลุมใบสั่งขายแรกจากสินค้าคงคลังคงเหลือที่มีอยู่และใบสั่งซื้อเพิ่มเติม สำหรับปริมาณเหลืออยู่

[![FEFO 1](media/FEFO1.png)](media/FEFO1.png)

มีการสร้างใบสั่งที่วางแผนไว้เพื่อให้แน่ใจว่า สินค้าคงคลังที่พร้อมใช้งานจะถูกเลื่อนกลับมายังขีดจำกัดความปลอดภัย

[![FEFO 2](media/FEFO2.png)](media/FEFO2.png)

เมื่อมีการวางแผนใบสั่งขายที่สอง ใบสั่งที่วางแผนไว้ซึ่งสร้างขึ้นก่อนหน้านี้ที่ครอบคลุมสินค้าคงคลังที่ปลอดภัย จะถูกใช้เพื่อครอบคลุมปริมาณนี้ ดังนั้น สินค้าคงคลังที่ปลอดภัยกำลังรวมตัวอย่างสม่ำเสมอ

[![FEFO 3](media/FEFO3.png)](media/FEFO3.png)

ในตอนท้าย มีการสร้างใบสั่งอื่นที่วางแผนไว้เพื่อครอบคลุมสินค้าคงคลังที่ปลอดภัย

[![FEFO 4](media/FEFO4.png)](media/FEFO4.png)

ชุดงานทั้งหมดหมดอายุตามลำดับ และมีการสร้างใบสั่งที่วางแผนไว้เพื่อเติมสินค้าคงคลังที่ปลอดภัย หลังจากที่หมดอายุแล้ว

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>วิธีที่การวางแผนหลักจัดการข้อจำกัดสินค้าคงคลังด้านความปลอดภัย

สินค้าคงคลังที่ปลอดภัยถูกติดตามในระบบเป็นความต้องการชนิด ลักษณะเดียวกับรายการขายหรือความต้องการ BOM คุณสามารถดูรายการความต้องการสินค้าคงคลังที่ปลอดภัยได้ในหน้า **ความต้องการสุทธิ** ถ้าคุณลบตัวกรองข้อมูลเริ่มต้นในคอลัมน์ **ชนิดความต้องการ** ออก

การเติมสินค้าธุรกรรมความต้องการสินค้าคงคลังที่ปลอดภัยจะถูกลดระดับความสำคัญ ถ้าระบบกำหนดว่าจะทำให้ความล่าช้าในการเติมสินค้าของความต้องการจริง เช่น รายการขาย รายการ BOM ความต้องการโอนย้าย หรือรายการการคาดการณ์ความต้องการ มิฉะนั้น การทำให้แน่ใจว่า สินค้าคงคลังที่พร้อมใช้งานอยู่สูงกว่าปริมาณสินค้าคงคลังที่ปลอดภัย มีระดับความสำคัญเดียวกันเป็นชนิดความต้องการอื่นๆ ซึ่งช่วยให้มั่นใจไม่มีความล่าช้าสำหรับธุรกรรมที่แท้จริง และช่วยในการป้องกันการเพิ่มเติมสินค้ามากกว่าปริมาณที่กำหนดและการเติมสินค้าก่อนกำหนดของสินค้าคงคลังที่ปลอดภัย

ในระหว่างขั้นตอนความครอบคลุมของการวางแผนหลัก ไม่มีการลดระดับความสำคัญการเติมสินค้าคงคลังที่ปลอดภัยอีกต่อไป สามารถใช้สินค้าคงคลังคงเหลือ ก่อนชนิดความต้องการอื่นๆ ได้ สินค้าคงคลังในระหว่างการคำนวณความล่าช้า ตรรกะใหม่จะถูกเพิ่มไปที่บรรทัดการขายที่ล่าช้า ข้อกำหนดของบรรทัด BOM และทั้งหมดความต้องการ ชนิดอื่น ๆ เพื่อกำหนดว่า จะไม่สามารถส่งข้อความในเวลา ถ้ามีการใช้สินค้าคงคลังที่ปลอดภัย ถ้าระบบระบุว่า จะสามารถลดความล่าช้าได้โดยใช้สินค้าคงคลังที่ปลอดภัย จากนั้น รายการขายหรือรายการ BOM จะแทนที่ความครอบคลุมเริ่มต้นของพวกเขาด้วยสินค้าคงคลังที่ปลอดภัย แล้วระบบจะทริกเกอร์การเติมสินค้าสำหรับสินค้าคงคลังปลอดภัยแทน

ถ้าแผนหรือสินค้าไม่ได้ถูกตั้งค่าสำหรับการคำนวณที่ล่าช้า จากนั้นข้อจำกัดสินค้าคงคลังด้านความปลอดภัยจะมีระดับความสำคัญเดียวกันกับชนิดความต้องการอื่นๆ ซึ่งหมายความว่า ไม่มีการสำรองของสินค้าคงคลังคงเหลือและสินค้าคงคลังอื่นๆ ก่อนความต้องการชนิดอื่นๆ

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ใช้สมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัยเพื่ออัพเดตความครอบคลุมขั้นต่ำสำหรับสินค้า](safety-stock-journal.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
