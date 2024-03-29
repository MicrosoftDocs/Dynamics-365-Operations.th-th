---
title: ติดตามการเดินทางขาเข้าและการเดินทางของคอนเทนเนอร์จัดส่ง
description: บทความนี้อธิบายวิธีการที่คุณสามารถใช้หน้าการติดตามขาเข้า เพื่อติดตามความคืบหน้าของการเดินทางและการเดินทางของคอนเทนเนอร์จัดส่ง
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 17874f984945b27e036eafda841ec1fd95d345be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854368"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>ติดตามการเดินทางขาเข้าและการเดินทางของคอนเทนเนอร์จัดส่ง

[!include [banner](../../includes/banner.md)]

หน้า **Iการติดตามขาเข้า** ช่วยให้คุณติดตามความคืบหน้าของการเดินทางและการเดินทางของคอนเทนเนอร์จัดส่ง การเดินทางและการเดินทางแต่ละครั้งจะแบ่งตาม *กิจกรรม* ซึ่งแต่ละกิจกรรมจะมีแถวของตนเองบนหน้า คุณสามารถใช้หน้าเพื่อดูและป้อนวันที่ที่ประเมินและวันที่จริงตามกิจกรรม

โดยทั่วไป ขึ้นอยู่กับการตั้งค่าใน [ศูนย์ควบคุมการติดตามต้นทุนที่ประเมิน](delivery-information-setup.md#tracking-control-center)  กิจกรรมเหล่านี้จะแสดงวันที่เริ่มต้นที่ประเเมิน ที่ปลายทางสุดท้าย นอกจากนี้ยังขึ้นอยู่กับการตั้งค่า โดยปกติวันที่สุดท้ายจะอัปเดตวันที่จัดส่งหรือวันที่ยืนยันในบรรทัดใบสั่งซื้อ สำหรับบรรทัดใบสั่งโอน คุณสามารถตั้งระบบให้อัปเดตวันที่รับสินค้าได้

เมื่อต้องการเปิดหน้า **การติดตามขาเข้า** ให้ไปที่ **ต้นทุนแฝง \> การติดตาม \> การติดตามขาเข้า**

## <a name="filter-the-activities-list"></a>กรองรายการกิจกรรม

คุณสามารถใช้ฟิลด์ **การเดินทาง** และ **คอนเทนเนอร์จัดส่ง** ที่ด้านบนของหน้า **การติดตามขาเข้า** เพื่อกรองหน้าเพื่อให้แสดงเฉพาะกิจกรรมที่เกี่ยวข้องกับการเดินทางและ/หรือคอนเทนเนอร์จัดส่งที่เลือก

## <a name="update-tracking-information"></a>อัปเตดข้อมูลการติดตาม

เมื่อต้องการอัปเดตกำหนดการของการเดินทางหรือการเดินทาง ให้ป้อนวันที่เริ่มต้นของกิจกรรมแรก จากนั้นมีการอัปเดตวันที่สิ้นสุดที่ประเมินไว้ของกิจกรรมล่าสุด การตั้งค่าสำหรับแต่ละขา และเท็มเพลตการเดินทางใน [ศูนย์ควบคุมการติดตาม](delivery-information-setup.md#tracking-control-center) จะระบุระยะเวลารอคอยสินค้าโดยประมาณ วันที่สิ้นสุดที่ประเมินไว้จะใช้ระยะเวลารอคอยสินค้าจากวันที่เริ่มต้นของกิจกรรม จากนั้น เมื่อบันทึกวันที่สิ้นสุดจริง วันที่เริ่มต้นของกิจกรรมถัดไปจะถูกอัปเดตเป็นวันเดียวกันกับวันที่สิ้นสุดจริงของกิจกรรมก่อนหน้า มีการอัปเดตระยะเวลารอคอยสินค้าจริง เพื่อให้สามารถเปรียบเทียบและวิเคราะห์ได้ หมายเหตุเพิ่มเติมสามารถป้อนในฟิลด์ **หมายเหตุ** ได้

ลำดับของกิจกรรมในกริดจะกําหนดตามลำดับของขาในเท็มเพลตการเดินทางที่เกี่ยวข้อง หากลำดับของขาในการเดินทางที่แนบมีการเปลี่ยนแปลง การควบคุมการติดตามจะเปลี่ยนไปด้วย

คุณสามารถอัปเดตวันที่สำหรับคอนเทนเนอร์จัดส่งทั้งหมด โดยการเลือก **อัปเดตวันที่เริ่มต้น** หรือ **อัปเดตวันที่สิ้นสุดจริง** ในบานหน้าต่างการดำเนินการ หรือ คุณสามารถป้อนวันที่ต่อคอนเทนเนอร์จัดส่งในการจัดส่ง วิธีการนี้จะช่วยให้มีความยืดหยุ่นมากขึ้น เนื่องจากคอนเทนเนอร์สามารถแบ่งในสภาพแวดล้อมการเดินทางหลายรายการได้

## <a name="buttons-on-the-action-pane"></a>ปุ่มบนบานหน้าต่างการดำเนินการ

คุณสามารถใช้ปุ่มในบานหน้าต่างการดำเนินการของหน้า **การติดตามขาเข้า** เพื่อทำงานกับการเดินทางและการเดินทางขาเข้า ตารางต่อไปนี้อธิบายปุ่มที่พร้อมใช้งาน

| ปุ่ม | คำอธิบาย |
|---|---|
| แก้ไข | แก้ไขการเดินทางหรือการเดินทางของคอนเทนเนอร์จัดส่ง |
| สร้าง  | สร้างการเดินทางใหม่หรือการเดินทางของคอนเทนเนอร์จัดส่ง |
| Delete | ลบการเดินทางหรือการเดินทางของคอนเทนเนอร์จัดส่งที่เลือก |
| อัพเดตวันที่เริ่มต้น | อัปเดตวันที่เริ่มต้นของกิจกรรม สำหรับคอนเทนเนอร์ทั้งหมดในการเดินทาง เมื่อวันที่เริ่มต้นของกิจกรรมหรือขาของการเดินทางมีการอัปเดต วันที่เริ่มต้นที่ประเมินในเวลาต่อมาจะถูกอัปเดตตามระยะเวลารอคอยสินค้าที่ระบุ |
| อัพเดตวันที่สิ้นสุดจริง | อัปเดตวันที่สิ้นสุดของกิจกรรม สำหรับคอนเทนเนอร์ทั้งหมดในการเดินทาง เมื่อวันที่สิ้นสุดของกิจกรรมที่ระบุมีการอัปเดต กิจกรรมต่อมาจะถูกอัปเดตตามระยะเวลารอคอยสินค้าที่ระบุ |
| เพิ่มกิจกรรม | การเพิ่มกิจกรรมในการเดินทางด้วยตนเอง ตัวอย่างเช่น คุณอาจเพิ่มกิจกรรมชั่วคราว กิจกรรมที่เพิ่มอาจทําให้วันที่จัดส่งสินค้าที่ยืนยันในเรือหรือการเดินทางมีการเปลี่ยนแปลง เมื่อเพิ่มกิจกรรมให้กับการเดินทาง วันที่ประเมินจะไม่ถูกป้อนจนกว่าวันที่เริ่มต้นของช่วงการเดินทางจะถูกอัปเดต |

## <a name="information-and-settings-on-the-overview-tab"></a>ข้อมูลและการตั้งค่าบนแท็บภาพรวม

แท็บ **ภาพรวม** จะแสดงรายการกิจกรรมทั้งหมดที่เป็นของการเดินทาง และ/หรือ คอนเทนเนอร์จัดส่งที่เลือกที่ด้านบนของหน้า ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับกิจกรรมแต่ละรายการ

| ฟิลด์ | คำอธิบาย |
|---|---|
| ช่วง | รหัสขาของกิจกรรม ตามที่กําหนดโดยเท็มเพลตการเดินทาง |
| วิธีการนำส่ง | วิธีการจัดส่งที่คาดไว้สำกรับกิจกรรม |
| กิจกรรม | โดยปกติฟิลด์นี้จะกำหนดงานหรืองานที่สัมพันธ์กับกิจกรรม ตัวอย่างทั่วไป ได้แก่ *การเดินเรือ* และ *การขายล้างสต๊อก* |
| คำอธิบาย | คำอธิบายรายละเอียดของกิจกรรม |
| วันที่เริ่มต้น | ฟิลด์นี้จะแสดงวันที่เริ่มต้นที่ประเมินไว้ของกิจกรรม อย่างไรก็ตาม หลังจากที่ป้อนวันที่สิ้นสุดจริงของกิจกรรมก่อนหน้าแล้ว วันที่เริ่มต้นจะแสดงวันที่เริ่มต้นจริง ฟิลด์นี้ใช้ในการระบุวันที่สิ้นสุดที่ประเมินไว้ ตามระยะเวลารอคอยสินค้า |
| ประเมินวันที่สิ้นสุด | ค่าของฟิลด์นี้จะคํานวณตามวันที่เริ่มต้นและระยะเวลารอคอยสินค้า โดยปกติแล้วคุณจะแก้ไขค่าโดยตรงไม่ได้ |
| วันที่สิ้นสุดจริง | ผู้ใช้ควรจะอัปเดตฟิลด์นี้ทันทีหลังจากที่กิจกรรมเกิดขึ้น จากนั้นระยะเวลารอคอยสินค้าจริงจะถูกอัปเดต |
| จำนวนวันที่ประเมิน | ระยะเวลาที่คาดไว้ (เป็นจำนวนวัน) ที่จำเป็นในการดำเนินการกิจกรรม |
| จำนวนวันจริง | ระยะเวลาจริง (เป็นจำนวนวัน) ที่จำเป็นในการดำเนินการกิจกรรม |
| บันทึกย่อ | ใช้ฟิลด์นี้เพื่อเพิ่มหมายเหตุเบ็ดเตล็ด และรายละเอียดเกี่ยวกับกิจกรรม |

## <a name="information-and-settings-on-the-general-tab"></a>ข้อมูลและการตั้งค่าบนแท็บทั่วไป

แท็บ **ทั่วไป** จะแสดงข้อมูลเกี่ยวกับขาที่เลือกบนเท็บ **ภาพรวม** ถึงแม้ว่าข้อมูลจะทําซ้ําบางข้อมูลที่จะปรากฏขึ้นบนแท็บ **ภาพรวม** แต่ก็รวมถึงข้อมูลเพิ่มเติมเกี่ยวกับขาที่เลือกด้วย
