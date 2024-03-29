---
title: ข้อเสนอการจัดการเงินคืน
description: บทความนี้จะอธิบายถึงวิธีการสร้างข้อตกลงการจัดการเงินคืน ข้อตกลงนี้ใช้ในการควบคุมวิธีการและฐานที่แตกต่างกันในการคํานวณเงินคืนและค่าลิขสิทธิ์ โดยรวมกฎไว้เพื่อรวมไว้ในการรวมและข้อยกเว้น
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 28cfff69ab4e528c146ccbf6a34548a819c99522
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851607"
---
# <a name="rebate-management-deals"></a>ข้อตกลงการจัดการเงินคืน

[!include [banner](../includes/banner.md)]

ข้อตกลงการจัดการเงินคืนนี้ใช้ในการควบคุมวิธีการและฐานที่แตกต่างกันในการคํานวณเงินคืนและค่าลิขสิทธิ์ โดยรวมกฎไว้เพื่อรวมไว้ในการรวมและข้อยกเว้น มีข้อตกลงการจัดการเงินคืนสามชนิดได้แก่ เงินคืนของลูกค้า ค่าสิทธิของลูกค้า และเงินคืนจากผู้จัดจำหน่าย ทั้งสามชนิดจะใช้การตั้งค่าที่คล้ายกัน บทความนี้จะชี้ความแตกต่างจากจุดที่มีอยู่

## <a name="create-a-deal"></a>สร้างข้อตกลง

1. ไปที่ **ข้อตกลงการจัดการ \> ข้อตกลงการจัดการเงินคืน \> ข้อตกลงการจัดการเงินคืนทั้งหมด** ในหน้ารายการ **ข้อตกลงการจัดการเงินคืนทั้งหมด** คุณสามารถสร้างและใช้งานข้อตกลงทั้งสามชนิดได้

    หรือทำตามหนึ่งในขั้นตอนเหล่านี้ ในแต่ละกรณี หน้ารายการที่จะปรากฏขึ้นมีการตั้งค่าทั้งหมดเดียวกันกับหน้ารายการ **ข้อตกลงการจัดการเงินคืนทั้งหมด** แต่จะมีการกรองเพื่อแสดงข้อตกลงที่มีชนิดเพียงชนิดเดียว

    - ไปที่ **การจัดการเงินคืน \> ข้อตกลงการจัดการเงินคืน \> ข้อตกลงเงินคืนของลูกค้า** เพื่อสร้างเฉพาะข้อตกลงเงินคืนของลูกค้า
    - ไปที่ **การจัดการเงินคืน \> ข้อตกลงการจัดการเงินคืน \> ข้อตกลงลิขสิทธิ์ของลูกค้า** เพื่อสร้างเฉพาะข้อตกลงลิขสิทธิ์ของลูกค้า
    - ไปที่ **การจัดการเงินคืน \> ข้อตกลงการจัดการเงินคืน \> ข้อตกลงเงินคืนของผู้จัดจำหน่าย** เพื่อสร้างเฉพาะข้อตกลงเงินคืนของผู้จัดจำหน่าย

1. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
1. ในกล่องโต้ตอบ **สร้างข้อตกลงใหม่** ให้ตั้งค่าฟิลด์ต่อไปนี้:

    - **ข้อตกลงการจัดการเงินคืน** – ถ้าคุณได้ [ตั้งค่าลำดับหมายเลข](rebate-management-parameters.md) ของข้อตกลงเงินคืนไว้ ระบบจะตั้งค่าฟิลด์นี้เป็นรหัสเฉพาะที่ระบบสร้างขึ้นโดยอัตโนมัติ มิฉะนั้น ป้อนรหัสเฉพาะ
    - **คำอธิบาย** – ป้อนคำอธิบายของข้อตกลง
    - **โมดูล** – เลือกชนิดของคู่ค้าที่จะใช้กับข้อตกลง (*ลูกค้า* หรือ *ผู้จัดจำหน่าย*) ขึ้นอยู่กับหน้าที่คุณเริ่มต้น ฟิลด์นี้อาจถูกตั้งค่าโดยอัตโนมัติตามชนิดข้อตกลงที่เลือก ในกรณีนี้ ฟิลด์นี้เป็นแบบอ่านอย่างเดียว
    - **ชนิด** – เลือกชนิดของข้อตกลง (*เงินคืน* หรือ *ค่าลิขสิทธิ์*) ขึ้นอยู่กับหน้าที่คุณเริ่มต้น ฟิลด์นี้อาจถูกตั้งค่าโดยอัตโนมัติตามชนิดข้อตกลงที่เลือก ในกรณีนี้ ฟิลด์นี้เป็นแบบอ่านอย่างเดียว
    - **กระทบยอดตาม** – เลือกวิธีการคํานวณและกระทบยอดข้อตกลงดังนี้:

        - *ข้อตกลง* – เงินคืนรายการเดียวควรมีการประมวลผลคืนเงินและการหักลดทั้งหมดในข้อตกลงนี้
        - *รายการ* – ควรมีการประมวลผลเงินคืนของแต่ละบรรทัดในข้อตกลง

    - **โปรไฟล์การลงบัญชี** – เลือก [โปรไฟล์การลงบัญชี](rebate-management-posting.md) ที่จะใช้ในธุรกรรมที่ข้อตกลงใช้ ฟิลด์นี้จะพร้อมใช้งานเฉพาะเมื่อตั้งค่าฟิลด์ **การกระทบยอดตาม** เป็น *ข้อตกลง* เท่านั้น ถ้ามีการกําหนดเป็น *รายการ* คุณจะกําหนดโปรไฟล์ในภายหลัง ให้กับแต่ละบรรทัดที่คุณเพิ่มในข้อตกลง
    - **โปรไฟล์การลงบัญชีสำหรับค้ำประกัน** – เลือก [โปรไฟล์การลงบัญชี](rebate-management-posting.md) ที่จะใช้ในธุรกรรมค้ำประกัน โปรไฟล์การลงรายการบัญชีเป็นข้อมูลที่ต้องระบุในธุรกรรมหนังสือค้ําประกันเฉพาะเมื่อหนังสือค้ําประกันใช้กับสมาชิกเท่านั้น มิฉะนั้น ถึงแม้ว่าโปรไฟล์การลงบัญชีจะไม่บังคับ ถ้าไม่ได้ระบุโพรไฟล์การลงรายการบัญชีไว้ ข้อผิดพลาดจะแสดงขึ้นเมื่อลงรายการบัญชีการค้ําประกัน ฟิลด์นี้จะพร้อมใช้งานเฉพาะเมื่อตั้งค่าฟิลด์ **ชนิด** เป็น *ลิขสิทธิ์* เท่านั้น 
    - **ผลลัพธ์เงินคืน** – เลือกวิธีชําระเงินคืนหรือค่าลิขสิทธิ์:

        - *การเงิน* – สร้างใบลดหนี้หรือใบเพิ่มหนี้ของบัญชีเจ้าหนี้ เพื่อให้ชําระเงินหรือได้รับชําระเงินในภายหลังได้ โปรดทราบว่าส่วนสำรอง **สามารถ** ใช้กับเงินคืนที่มีการเลือกตัวเลือกนี้ไว้ ตัวเลือกนี้พร้อมใช้งานเฉพาะเมื่อตั้งค่าฟิลด์ **ชนิด** เป็น *ลิขสิทธิ์* เท่านั้น
        - *สินค้า* – สร้างใบสั่งขายให้กับสินค้าตามการตั้งค่าข้อตกลง ในใบสั่งขายนี้ ราคา 0 (ศูนย์) ถูกมอบหมายให้กับสินค้าแต่ละรายการ โปรดทราบว่าส่วนสำรอง **ไม่สามารถ** ใช้กับเงินคืนที่มีการเลือกตัวเลือกนี้ไว้

    - **สกุลเงินเงินคืน** – เลือกสกุลเงินที่จะใช้เมื่อชําระเงินคืน การหักเงิน หรือค่าลิขสิทธิ์
    - **บันทึกเอกสาร** – ป้อนหมายเหตุเกี่ยวกับข้อตกลงตามที่ต้องการ
    - **ค้ำประกันสะสม** – คุณสามารถตั้งค่าตัวเลือกนี้เป็น *ใช่* เมื่อฟิลด์ **ชนิด** ถูกตั้งค่าเป็น *ลิขสิทธิ์* ตัวเลือกนี้มีผลกระทบต่อการคํานวณการหักลดที่รับประกัน นี่คือตัวอย่าง:

        - การค้ําประกันของข้อตกลงคือการขายมูลค่าที่จะไปสู่การชำระเงิน $10,000 ต่อไตรมาส
        - องค์กรที่ขายสินค้าขายมูลค่าที่ส่งผลให้การหักเงิน $12,000 อยู่ในไตรมาส 1 ผลลัพธ์คือค่าลิขสิทธิ์ $12,000 ที่ชําระ ลบด้วยค้ำประกัน $10,000
        - ถ้าตั้งค่า **ค้ำประกันสะสม** ตั้งค่าเป็น *ใช่* ค่าลิขสิทธิ์อีก $2,000 ที่ได้รับค่าจ้างในไตรมาส 1 จะใช้กับไตรมาสที่ 2 ดังนั้นลูกค้าจึงได้รับค้ำประกัน $8,000 (ค้ำประกัน $10,000 ลบการชำระเงิน $2,000 เพิ่มเติม)
        - ในไตรมาสที่ 2 คุณลงทะเบียนการขายที่ทริกเกอร์ค่าลิขสิทธิ์ $5,000
        - ระบบระบุการชําระเงิน $3,000 (ค้ําประกัน $8,000 ลบด้วย $5,000 ของค่าลิขสิทธิ์ที่ชําระแล้ว)
        - ถ้าตั้งค่าตัวเลือก **ค้ำประกันสะสม** เป็น *ไม่* จะได้รับการประกัน $10,000 ในแต่ละไตรมาส หนังสือค้ําประกันนี้จะตรงกับการชําระเงิน $5,000 ในไตรมาส 2 (การค้ําประกัน $10,000 ลบด้วย $5,000 ค่าลิขสิทธิ์ที่ชําระแล้ว)

1. เลือก **ตกลง** เพื่อสร้างข้อตกลง และปิดกล่องโต้ตอบ

กระบวนงานนี้จะสร้างระดับหัวข้อของข้อตกลงใหม่ จากนั้น คุณจะสามารถเพิ่มรายการในข้อตกลงได้

## <a name="add-lines-to-a-deal"></a>การเพิ่มรายการในข้อตกลง

หลังจากที่คุณสร้างข้อตกลงตามที่อธิบายไว้ในส่วนก่อนหน้านี้แล้ว คุณสามารถเปิดข้อตกลงนี้จากหน้ารายการได้ จากนั้นคุณสามารถเพิ่มบรรทัดเพื่อระบุลูกค้าหรือผู้ขาย สินค้า กรอบเวลา เกณฑ์พื้นฐาน และวิธีการคํานวณข้อตกลงได้ ข้อตกลงอาจมีรายการเพียงรายการเดียวหรือหลายรายการ ถ้าข้อตกลงมีหลายรายการ โดยทั่วไปข้อตกลงจะมีชนิดเดียวกัน หรือมีการเชื่อมโยงพารามิเตอร์เดียวกัน จนกว่าคุณจะเพิ่มรายการในข้อตกลง ข้อตกลงจะไม่มีผลใด ๆ

1. เปิดหน้ารายการข้อตกลงเงินคืนที่เหมาะสม ตามที่อธิบายไว้ในส่วนก่อนหน้านี้
1. ค้นหาและเปิดข้อตกลงที่คุณต้องการใช้งาน
1. บนแท็บด่วน **การจัดการเงินคืน** ให้เลือกปุ่มใดปุ่มหนึ่งต่อไปนี้เพื่อเพิ่มบรรทัดข้อตกลงในกริด

    - **เพิ่มรายการ** – เพิ่มรายการข้อตกลงใหม่ที่ว่างเปล่า
    - **คัดลอกรายการ** – ถ้าบรรทัดข้อตกลงที่มีอยู่คล้ายกับบรรทัดข้อตกลงที่คุณต้องการเพิ่ม คุณสามารถเลือกปุ่มนี้เพื่อคัดลอกเพิ่มสําเนาของบรรทัดนั้น รายการข้อตกลงใหม่จะรวมการตั้งค่าทั้งหมดจากรายละเอียดการจัดการเงินคืนที่เกี่ยวข้อง จากนั้นคุณก็สามารถแก้ไขการตั้งค่าได้ ตัวอย่างเช่น โดยปกติแล้วคุณจะอัพเดตความสัมพันธ์ของสินค้าและเปอร์เซ็นต์เงินคืน

1. ในรายการข้อตกลงใหม่ ตั้งค่าฟิลด์ต่อไปนี้:

    - **หมายเลขการจัดการเงินคืน** – ถ้าคุณได้ [ตั้งค่าลำดับหมายเลข](rebate-management-parameters.md) ของหมายเลขการจัดการเงินคืน ระบบจะตั้งค่าฟิลด์นี้เป็นรหัสเฉพาะที่ระบบสร้างขึ้นโดยอัตโนมัติ มิฉะนั้น ป้อนรหัสเฉพาะ
    - **ชนิด** – ชนิดของข้อตกลงที่ใช้กับรายการ (*เงินคืน* หรือ *ค่าลิขสิทธิ์*) ค่าถูกคัดลอกจากส่วนหัวไม่สามารถเปลี่ยนแปลงได้
    - **คำอธิบาย** – ป้อนคำอธิบายของรายการข้อตกลง
    - **บริษัท** – เลือกบริษัท (นิติบุคคล) ที่จะใช้รายการข้อตกลง ในระหว่างการประมวลผล ผู้ใช้สามารถประมวลผลได้เฉพาะรายการข้อตกลงที่มอบหมายให้กับบริษัทที่ปัจจุบันใช้อยู่เท่านั้น หน้ารายการ **ข้อตกลงเงินคืนของลูกค้า** มีมุมมองแบบหลายบริษัท ตามสิทธิ์ความปลอดภัยของผู้ใช้ อย่างไรก็ตาม คุณสามารถแก้ไขและประมวลผลเงินคืนของบริษัทที่คุณใช้อยู่ในปัจจุบันเท่านั้น
    - **รหัสบัญชี** – เลือกขอบข่ายของลูกค้าหรือผู้ขายที่จะใช้กับรายการข้อตกลงดังนี้

        - *ตาราง* – รายการข้อตกลงจะใช้กับลูกค้าหรือผู้จัดจำหน่ายเฉพาะราย
        - *กลุ่ม* – รายการข้อตกลงจะใช้กับกลุ่มของลูกค้าหรือผู้จัดจำหน่าย สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่ากลุ่ม ให้ดูที่ [กลุ่มการจัดการเงินคืน](rebate-management-groups.md)
        - *ทั้งหมด* – รายการข้อตกลงจะใช้กับลูกค้าหรือผู้จัดจำหน่ายทั้งหมด

    - **ความสัมพันธ์บัญชี** – ถ้าคุณเลือก *ตาราง* ในฟิลด์ **รหัสบัญชี** เลือกลูกค้าหรือผู้จัดจำหน่ายที่ใช้ข้อตกลง ถ้าคุณเลือก *กลุ่ม* ให้เลือกกลุ่มลูกค้าหรือผู้จัดจำหน่าย หากคุณเลือก *ทั้งหมด* จะไม่มีฟิลด์นี้
    - **รหัสสินค้า** – เลือกขอบข่ายของสินค้าที่จะใช้กับรายการข้อตกลงดังนี้

        - *ตาราง* – รายการข้อตกลงจะใช้กับสินค้าเฉพาะ
        - *กลุ่ม* – รายการข้อตกลงจะใช้กับกลุ่มของสินค้า สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่ากลุ่ม ให้ดูที่ [กลุ่มการจัดการเงินคืน](rebate-management-groups.md)
        - *ทั้งหมด* – รายการข้อตกลงจะใช้กับสินค้าทั้งหมด

    - **ความสัมพันธ์ของสินค้า** – ถ้าคุณเลือก *ตาราง* ในฟิลด์ **รหัสของสินค้า** เลือกสินค้าที่ใช้รายการข้อตกลง ถ้าคุณเลือก *กลุ่ม* ให้เลือกกลุ่มสินค้า หากคุณเลือก *ทั้งหมด* จะไม่มีฟิลด์นี้
    - **ชนิดของหน่วย** – เลือกชนิดหน่วยที่ใช้กับบรรทัดการจัดการ (*หน่วยสินค้าคงคลัง* หรือ *หน่วยตามน้ำหนักจริง*) โปรดทราบว่าฟิลด์นี้อาจว่างเปล่าสําหรับเรกคอร์ดที่เก่ากว่า ในกรณีนี้ จะมีการสมมติค่า *หน่วยสินค้าคงคลัง*
    - **(พารามิเตอร์การบริหารสินค้าคงคลัง)** – ในฟิลด์ที่เหลือในบรรทัดข้อตกลง ให้ระบุค่าให้กับพารามิเตอร์การบริหารสินค้าคงคลังที่จะใช้ในการกําหนดสินค้าที่รวมอยู่ในข้อตกลงนั้น (เช่น ขนาดของสินค้า สี ลักษณะ ไซต์ และคลังสินค้า) เมื่อต้องการเพิ่มหรือลบมิติ ให้เลือก **แสดงมิติ** ในบานหน้าต่างการดำเนินการ

1. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**
1. ถ้าคุณต้องการจํากัดชุดสินค้าที่รายการข้อตกลงใช้ต่อไป ให้เลือกรายการ จากนั้นบนแท็บด่วน **การจัดการเงินคืน** ให้เลือก **ตัวกรอง** เพื่อเปิดกล่องโต้ตอบ **การสอบถาม** มาตรฐาน
1. ตั้งค่ารายละเอียดการคํานวณและรายละเอียดอื่นๆ บนแท็บด่วน **รายละเอียดการจัดการเงินคืน** ตามที่อธิบายไว้ในส่วนถัดไป

## <a name="add-rebate-management-details-to-a-deal-line"></a>เพิ่มรายละเอียดการจัดการเงินคืนให้กับรายการข้อตกลง

สำหรับแต่ละรายการในข้อตกลงของคุณ คุณต้องตั้งค่ารายละเอียดบนแท็บด่วน **รายละเอียดการจัดการเงินคืน** ก่อนอื่นให้เลือกรายการข้อตกลงบนแท็บด่วน **การจัดการเงินคืน** จากนั้นตั้งค่าบรรทัดข้อตกลงนั้นโดยใช้แท็บต่างๆ บนแท็บด่วน **รายละเอียดการจัดการเงินคืน** ส่วนย่อยต่อไปนี้อธิบายถึงวิธีใช้แต่ละแท็บ

### <a name="settings-on-the-general-tab"></a>การตั้งค่าบนแท็บทั่วไป

แท็บ **ทั่วไป** บนแท็บด่วน **รายละเอียดการจัดการเงินคืน** ช่วยให้คุณตั้งค่าวิธีการคํานวณและเกณฑ์พื้นฐานเกี่ยวกับรายการข้อตกลงที่เลือก การตั้งค่านี้จะควบคุมว่าต้องมีการซื้อขั้นต่ำสุดหรือไม่ โปรไฟล์การลงบัญชีที่สัมพันธ์กับบรรทัดข้อตกลง และรายละเอียดของการคํานวณ ตารางต่อไปนี้อธิบายถึงฟิลด์ที่มีอยู่

| ฟิลด์ | คำอธิบาย |
|---|---|
| วิธีการคำนวณ | เลือกวิธีการที่จะใช้เมื่อรายการข้อตกลงที่เลือกถูกรวมกับรายการข้อตกลงอื่นๆ (*เพิ่มขึ้นตามขั้น* *สะสม* *ย้อนหลัง* หรือ *รวม*) ค่าของฟิลด์นี้อาจมีผลกระทบต่อผลลัพธ์ของการคํานวณเงินคืนของคุณ หากต้องการอธิบายวิธีการแต่ละวิธีและตัวอย่างที่แสดงให้เห็นว่าวิธีการคํานวณเงินคืนมีผลอย่างไร โปรดดูส่วน [วิธีการคํานวณรายการข้อตกลง](#calc-methods) ในภายหลังในบทความนี้ |
| ข้อมูลพื้นฐาน | เลือกว่าจะใช้เงินคืนตามปริมาณ (นั่นคือจํานวนรวมของหน่วยที่ซื้อหรือขาย) หรือมูลค่า (นั่นคือราคารวมของสินค้าที่ซื้อหรือขาย) |
| ชนิดธุรกรรม | <p>เลือกจุดในกระบวนการเมื่อการคํานวณควรเกิดขึ้นดังนี้</p><ul><li>*ใบสั่ง* – ใช้ปริมาณหรือค่าที่สั่งเป็นข้อมูลพื้นฐานในการคํานวณ</li><li>*ที่จัดส่ง* – ใช้ปริมาณหรือค่าที่จัดส่งเป็นข้อมูลพื้นฐานในการคํานวณ</li><li>*ใบแจ้งหนี้* – ใช้ปริมาณหรือค่าที่ออกใบแจ้งหนี้เป็นข้อมูลพื้นฐานในการคํานวณ</li></ul> |
| หน่วย | ถ้าคุณเลือก *ปริมาณ* ในฟิลด์ **ข้อมูลพื้นฐาน** ให้เลือกหน่วยที่ต้องระบุปริมาณ |
| ยอดต่ำสุด | ป้อนยอดเงินต่สุดที่ต้องชําระต่อรอบระยะเวลา คุณสามารถป้อนค่าลบเพื่ออนุญาตให้ใช้ยอดเงินคืนค่าลบถ้าใบลดหนี้เกินยอดขายของรอบระยะเวลา |
| หลักการลดเงินคืน | เลือก [หลักการลดเงินคืน](rebate-reduction-principle.md) ที่จะใช้กับรายการข้อตกลงดังนี้ |
| หมายเลขตัวแปร | ถ้ารายการข้อตกลงใช้กับสินค้าที่มีตัวแปร ให้เลือกตัวแปรที่จะใช้กับรายการข้อตกลง |
| เกณฑ์เงินคืนของผู้จัดจำหน่าย | <p>ฟิลด์นี้จะแสดงเฉพาะเงินคืนจากผู้จัดจำหน่ายเท่านั้น (นั่นคือข้อตกลงที่มีการตั้งค่าฟิลด์ **โมดูล** เป็น *ผู้จัดจำหน่าย*) เลือกเกณฑ์สำหรับเงินคืนของผู้จัดจำหน่าย:</p><ul><li>*ใบสั่งซื้อ* – เงินคืนที่ผู้จัดการขายได้รับขึ้นอยู่กับปริมาณหรือมูลค่าในใบสั่งซื้อ</li><li>*ใบสั่งขาย* – ผู้ขายได้รับเงินคืนเฉพาะหลังจากที่ขายสินค้าแล้วเท่านั้น เงินคืนขึ้นอยู่กับปริมาณหรือค่าของใบสั่งขาย</li></ul> |
| ฐานราคา | <p>ฟิลด์นี้จะแสดงเฉพาะเงินคืนจากผู้จัดจำหน่ายเท่านั้น (ข้อตกลงที่มีการตั้งค่าฟิลด์ **โมดูล** เป็น *ผู้จัดจำหน่าย*) ถ้าคุณเลือก *ใบสั่งขาย* ในฟิลด์ **เกณฑ์เงินคืนของผู้จัดจำหน่าย** ให้เลือกเกณฑ์ราคาที่เกี่ยวข้องดังนี้</p><ul><li><p>*FIFO* – งานประจำงวด **คํานวณราคาซื้อ FIFO** ต้องทำงานเพื่อคำนวณเงินคืน (เมื่อต้องการรันงาน ให้ไปที่ **การจัดการเงินคืน \> งานประจำงวด \> คำนวณราคาซื้อ FIFO**) กฎแบบเข้าก่อนออกก่อน (FIFO) จะถูกใช้เพื่อคํานวณมูลค่าของสินค้าคงคลังที่ขาย จากนั้นค่านี้จะใช้ในการคํานวณเงินคืนให้แก่ผู้จัดจำหน่าย นี่คือตัวอย่าง:</p><ul><li>**สินค้าคงคลังที่ขาย:** 1,000 หน่วยที่ $3.00 ต่อหน่วย = $3,000</li><li>**ราคาซื้อปัจจุบัน ขึ้นอยู่กับ FIFO:** $2.00</li><li>**การคํานวณการทำงาน:** *จำนวนหน่วยที่ขาย* × *ราคาซื้อปัจจุบัน* = 1,000 × $2.00 = $2,000</li></ul></li><li><p>*ราคาซื้อล่าสุด* – ค่าจากธุรกรรมการซื้อล่าสุดจะถูกใช้เพื่อคํานวณเงินคืนจากผู้จัดจำหน่าย นี่คือตัวอย่าง:</p><ul><li>**สินค้าคงคลังที่ขาย:** 1,000 หน่วยที่ $3.00 ต่อหน่วย = $3,000</li><li>**ราคาซื้อล่าสุด:** $2.00</li><li>**การคํานวณการทำงาน:** *จำนวนหน่วยที่ขาย* × *ราคาซื้อล่าสุด* = 1,000 × $2.00 = $2,000</li></ul></li><li><p>*ราคาซื้อเฉลี่ย* – มูลค่าเฉลี่ยถ่วงน้ําหนัก *X* เดือนสุดท้ายจะได้รับการใช้ในการคํานวณเงินคืนจากผู้จัดซื้อ ถ้าคุณเลือกตัวเลือกนี้ คุณต้องป้อนจํานวนเดือนในฟิลด์ **จํานวนเดือน** (ซึ่งจะพร้อมใช้งานเฉพาะเมื่อตั้งค่าฟิลด์ **ฐานราคา** เป็น *ราคาซื้อเฉลี่ย*) นี่คือตัวอย่าง:</p><ul><li>**สินค้าคงคลังที่ขาย:** 1,000 หน่วยที่ $3.00 ต่อหน่วย = $3,000</li><li>**ราคาซื้อเฉลี่ย:** $2.00</li><li>**การคํานวณการทำงาน:** *จำนวนหน่วยที่ขาย* × *ราคาซื้อเฉลี่ย* = 1,000 × $2.00 = $2,000</li></ul></li><li><p>*ราคาขาย* – ราคาขายจะใช้เพื่อคํานวณเงินคืนจากผู้จัดจำหน่าย นี่คือตัวอย่าง:</p><ul><li>**สินค้าคงคลังที่ขาย:** 1,000 หน่วยที่ $3.00 ต่อหน่วย = $3,000</li><li>**ราคาซื้อเฉลี่ย:** $2.00</li><li>**การคํานวณการทำงาน:** *จำนวนหน่วยที่ขาย* × *ราคาขาย* = 1,000 × $3.00 = $3,000</li></ul></li></ul> |
| จำนวนของเดือน | ฟิลด์นี้จะแสดงเฉพาะเงินคืนจากผู้จัดจำหน่ายเท่านั้น (ข้อตกลงที่มีการตั้งค่าฟิลด์ **โมดูล** เป็น *ผู้จัดจำหน่าย*) ถ้าคุณเลือก *ราคาซื้อเฉลี่ย* ในฟิลด์ **ฐานราคา** ให้ป้อนจํานวนเดือนที่ควรจะใช้ |
| โพรไฟล์การลงรายการบัญชี | เลือก [โปรไฟล์การลงบัญชี](rebate-management-posting.md) ที่จะใช้กับรายการข้อตกลงที่เลือกนี้ โปรไฟล์นี้จะใช้เฉพาะเมื่อฟิลด์ **กระทบยอดตาม** บนส่วนหน้าของข้อตกลงถูกตั้งค่าเป็น *รายการ* ถ้ามีการตั้งค่าฟิลด์ **การกระทบยอดตาม** เป็น *ข้อตกลง* โปรไฟล์การลงบัญชีที่ตั้งค่าไว้ในหัวข้อข้อตกลงจะถูกใช้เสมอ ถ้าไม่มีการตั้งค่าโปรไฟล์การลงบัญชีเป็นรายการข้อตกลง โปรไฟล์การลงบัญชีที่ตั้งค่าไว้ในหัวข้อข้อตกลงจะถูกใช้เสมอ |
| โปรไฟล์การลงรายการบัญชีเพื่อค้ําประกัน | ฟิลด์นี้จะมีลักษณะเป็นฟิลด์ **โปรไฟล์การลงบัญชี** แต่จะใช้กับสมาชิกเท่านั้น |
| ชนิดของการชำระเงิน | ชนิดของการชำระเงินที่จะใช้สำหรับโปรไฟล์การลงบัญชีที่เลือกสำหรับข้อตกลง |
| ภาษีขายรวม | เลือกว่าธุรกรรมเป็นธุรกรรมรวมภาษีหรือไม่ ความรวมภาษีจะเกี่ยวข้องเฉพาะเมื่อฟิลด์ **ข้อมูลพื้นฐาน** ถูกตั้งค่าเป็น *ค่า* เท่านั้น ยอดเงินในใบแจ้งหนี้จะใช้เป็นยอดเงินรวมภาษี หากการคํานวณเงินคืนเป็นไปตามเปอร์เซ็นต์ ระบบจะคูณเปอร์เซ็นต์เงินคืนตามจํานวนเงินที่รวมภาษีไว้ โปรดทราบว่าการคํานวณจะใช้มูลค่าภาษีขายจากรายการข้อตกลง |
| รวมใบลดหนี้ | <p>ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อรวมใบลดหนี้ในการคํานวณเงินคืน</p><p>ถ้าคุณตั้งค่าตัวเลือกนี้เป็น *ใช่* ผลกระทบจะแตกต่างกันไป ขึ้นอยู่กับค่าของฟิลด์ **ชนิดของธุรกรรม** ดังนี้</p><ul><li>ถ้าฟิลด์ **ชนิดธุรกรรม** มีการตั้งค่าเป็น *ใบแจ้งหนี้* การคํานวณจะมีผลในใบลดหนี้ การตั้งค่าคอนฟิกนี้เป็นการตั้งค่าคอนฟิกปกติ</li><li>ถ้าฟิลด์ **ชนิดธุรกรรม** มีการตั้งค่าเป็น *ใบสั่ง* การคํานวณจะคูณในใบสั่งขายทั้งสองที่มีค่าลบและใบสั่งส่งคืนสินค้าที่เปิด</li></ul> |
| ยอดเงินที่คิดส่วนลด | ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อให้ระบบคํานวณตามยอดส่วนลดของสินค้าหรือสินค้า ในกรณีที่ได้รับส่วนลดต่อรายการสินค้า |
| ใบแจ้งหนี้ที่ชําระแล้วเท่านั้น | ตั้งค่าตัวเลือกนี้เป็น *ใช่* ถ้าการคํานวณควรพิจารณาเฉพาะใบแจ้งหนี้ที่ชําระเงินเต็มแล้วเท่านั้น (เงินคืนจะไม่ได้รับการคํานวณเป็นใบแจ้งหนี้ที่ชําระเงินบางส่วน) ตัวเลือกนี้จะพร้อมใช้งานเฉพาะเมื่อตั้งค่าฟิลด์ **ชนิดของธุรกรรม** เป็น *ใบแจ้งหนี้* เท่านั้น |
| รวมข้อความอิสระ | ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อรวมใบแจ้งหนี้ข้อความอิสระในการคํานวณเงินคืน สามารถรวมใบแจ้งหนี้ข้อความอิสระได้เฉพาะกับรายการข้อตกลงที่มีการตั้งค่าฟิลด์ **รหัสสินค้า** เป็น *ทั้งหมด* เท่านั้น |
| รวมส่วนลดในการชําระเงิน | ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อลดเงินคืนตามส่วนลดการชําระเงินครั้งแรก ระบบสมมติว่าองค์กรจะได้รับส่วนลดในการชําระเงินครั้งแรก ตั้งค่าตัวเลือกนี้เป็น *ไม่* เพื่อเปิดใช้งานส่วนลดในการชําระบัญชีที่จะใช้ในภายหลัง |
| บันทึกเอกสาร | ป้อนหมายเหตุที่ควรใช้เป็นข้อความธุรกรรมในบรรทัดสมุดรายวันธุรกรรมเงินคืน |

### <a name="settings-on-the-dates-tab"></a>การตั้งค่าบนแท็บวันที่

การตั้งค่าบนแท็บด่วน **วันที่** บนแท็บด่วน **รายละเอียดการจัดการเงินคืน** จะกําหนดความถี่และช่วงเวลาของการคํานวณที่ระบุไว้บนแท็บ **ทั่วไป** โดยจะตัดสินว่าการคํานวณจะเกิดขึ้นอย่างไรในเวลาที่ประมวลผล

แท็บนี้จะช่วยให้คุณสามารถระบุช่วงของวันที่ที่บรรทัดข้อตกลงที่เลือกมีผลใช้ได้ และความถี่ในการคํานวณ คุณยังสามารถระบุว่าควรลงรายการบัญชีการค้ําประกันหรือไม่ และเมื่อใด

คุณสามารถใช้ปุ่มบนแถบเครื่องมือเพื่อเพิ่มรายการวันที่ลงในกริด หรือเพื่อลบ ถ้ามีรายการวันที่หลายรายการ ช่วงวันที่ที่ถูกต้องต้องไม่ทับซ้อนกัน คุณจะได้รับข้อความแสดงข้อผิดพลาดเมื่อคุณพยายามบันทึกข้อตกลง

ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับสินค้าแต่ละรายการวันที่

| ฟิลด์ | คำอธิบาย |
|---|---|
| วันที่เริ่มต้น | ป้อนวันที่แรกที่จะใช้กับรายการวันที่ ถ้าวันที่ "เริ่มต้น" และ "สิ้นสุด" มีการระบุอยู่ในหัวข้อของข้อตกลง จะใช้ค่าเริ่มต้นนี้กับรายการวันที่ใหม่ทุกรายการ |
| วันที่สิ้นสุด | ป้อนวันที่สุดท้ายที่จะใช้กับรายการวันที่ ถ้าวันที่ "เริ่มต้น" และ "สิ้นสุด" มีการระบุอยู่ในหัวข้อของข้อตกลง จะใช้ค่าเริ่มต้นนี้กับรายการวันที่ใหม่ทุกรายการ |
| ต่อ | ระบุความถี่ที่ควรใช้ในการคำนวณรายการข้อตกลง ป้อนจํานวนเต็มที่นี่ แล้วเลือกหน่วยในฟิลด์ **สะสมตาม** ตัวอย่างเช่น เมื่อต้องการคํานวณทุกสัปดาห์ ให้ตั้งค่าฟิลด์ **ต่อ** เป็น *2* และฟิลด์ **สะสมตาม** เป็น *สัปดาห์* |
| สะสมตาม | เลือกหน่วยที่ใช้กับการตั้งค่า **ต่อ** เลือก *อายุการใช้งาน* เพื่อคํานวณอายุการใช้งานทั้งหมดของรายการข้อตกลง เลือก *รอบระยะเวลาที่กําหนด* เพื่อเลือกรอบระยะเวลาที่กําหนดไว้ในบัญชีแยกประเภททั่วไป ในกรณีนี้ คุณต้องตั้งค่าฟิลด์ **ชนิดของรอบระยะเวลา** ด้วย |
| ชนิดของรอบระยะเวลา | ฟิลด์นี้จะพร้อมใช้งานเฉพาะเมื่อตั้งค่าฟิลด์ **สะสมตาม** เป็น *รอบระยะเวลาที่กําหนด* เท่านั้น ค่าที่พร้อมใช้งานในการเลือกจะมาจากชนิดรอบระยะเวลาที่กําหนดไว้ในบัญชีแยกประเภททั่วไป |
| วันแรกของสัปดาห์ | ระบุว่าจะระบุสัปดาห์อย่างไรในรอบระยะเวลา ฟิลด์นี้จะพร้อมใช้งานเฉพาะเมื่อตั้งค่าฟิลด์ **สะสมตาม** เป็น *สัปดาห์* เท่านั้น |
| การอ้างสิทธิ์ต่อ | ระบุว่าจะอ้างสิทธิ์ส่วนลดเงินคืนได้บ่อยเท่าใดในรายการข้อตกลง ป้อนจํานวนเต็มที่นี่ แล้วเลือกหน่วยในฟิลด์ **อ้างสิทธิ์ตาม** |
| การอ้างสิทธิ์โดย | เลือกหน่วยที่ใช้กับการตั้งค่า **อ้างสิทธิ์ต่อ** เลือก *อายุการใช้งาน* เพื่ออนุญาตให้มีการอ้างสิทธิ์เพียงครั้งเดียวในระหว่างอายุการใช้งานทั้งหมดของรายการข้อตกลง เลือก *รอบระยะเวลาที่กําหนด* เพื่อเลือกรอบระยะเวลาที่กําหนดไว้ในบัญชีแยกประเภททั่วไป ในกรณีนี้ คุณต้องตั้งค่าฟิลด์ **ชนิดของรอบระยะเวลาการอ้างสิทธิ์** ด้วย |
| ชนิดรอบระยะเวลาการอ้างสิทธิ์ | ฟิลด์นี้จะพร้อมใช้งานเฉพาะเมื่อตั้งค่าฟิลด์ **อ้างสิทธิ์ตาม** เป็น *รอบระยะเวลาที่กําหนด* เท่านั้น ค่าที่พร้อมใช้งานในการเลือกจะมาจากชนิดรอบระยะเวลาที่กําหนดไว้ในบัญชีแยกประเภททั่วไป |
| กระบวนการการลงรายการบัญชี | เลือกกล่องกาเครื่องหมายนี้ถ้ารายการการอ้างสิทธิ์ควรประมวลผลระหว่างการลงรายการบัญชี ตัวเลือกนี้พร้อมใช้งานเฉพาะกับบรรทัดข้อตกลงที่มีการตั้งค่าฟิลด์ **ชนิดของธุรกรรม** บนแท็บ **ทั่วไป** เป็น *จัดส่งแล้ว* หรือ *ใบแจ้งหนี้* ส่วนสํารองจะลงรายการบัญชีส่วนสํารองเมื่อสร้างบันทึกการจัดส่งหรือใบแจ้งหนี้ |
| การค้ําประกันต่อ | ฟิลด์นี้จะใช้กับข้อตกลงของค่าลิขสิทธิ์เท่านั้น ระบุความถี่ในการคํานวณหนังสือค้ําประกันของสมาชิกในระหว่างรอบระยะเวลาที่กําหนดโดยการตั้งค่า **สะสมตาม** ป้อนจํานวนเต็มที่นี่ แล้วเลือกเวลาการชำระเงินในฟิลด์ **ค้ําประกันที่จ่ายแล้ว** |
| ค้ําประกันที่จ่ายแล้ว | <p>ฟิลด์นี้จะใช้กับข้อตกลงของค่าลิขสิทธิ์เท่านั้น โดยจะร่วมกับฟิลด์ **ประกันต่อ** เพื่อกําหนดความถี่ของการคํานวณหนังสือค้ําประกัน เลือกค่าใดค่าหนึ่งต่อไปนี้</p><ul><li><p>*จุดเริ่มต้นของรอบระยะเวลา* – หนังสือค้ําประกันจะจ่ายเมื่อเริ่มต้นรอบระยะเวลาข้อตกลงที่กําหนดไว้หมายถึงรายการวันที่ การรับประกันทั้งหมดจะถูกประมวลผลก่อน เฉพาะค่าของรางวัลที่เกินยอดเงินที่รับประกันเท่านั้นที่จะถูกลงรายการบัญชีเป็นของรางวัล นี่คือตัวอย่าง:</p><ul><li>**หนังสือค้ำประกันต่ำสุด** $10,000 ต่อสองเดือน</li><li>**เดือนที่ 1** $10,000 มีการลงรายการบัญชีการค้ําประกัน และ $0 รายการบัญชีสมาชิกแล้ว</li><li>**เดือนที่ 2** $2,000 มีการลงรายการบัญชีสมาชิก และ $0 รายการบัญชีการค้ําประกันแล้ว</li><li>**การคํานวณการทำงาน:** *ประกันที่เหลือ* – *ค่าลิขสิทธิ์ที่ลงรายการบัญชี* = $0 – $2,000 = -$2,000</li></ul><p>เนื่องจากต้องระบุการชำระเงิน $2,000 มีการสร้างสมุดรายวันของ $2,000</p><p>**หมายเหตุ:** ควรคํานวณและลงรายการบัญชีการค้ําประกันพร้อมกับส่วนสํารองการหักลดสําหรับรอบระยะเวลาแรก</p></li><li><p>*สิ้นสุดรอบระยะเวลา* – ไม่ชําระเงินค้ําประกันจนกว่าจะสิ้นสุดข้อตกลงการหักลด ตามที่กําหนดไว้ในรายการวันที่ นี่คือตัวอย่าง:</p><ul><li>**หนังสือค้ำประกันต่ำสุด** $10,000 ต่อสองเดือน</li><li>**เดือนที่ 1** $5,000 มีการลงรายการบัญชีสมาชิกและสมุดรายวันถูกสร้างขึ้นแล้ว</li><li>**เดือนที่ 2** $7,000 มีการลงรายการบัญชีสมาชิกและสมุดรายวันถูกสร้างขึ้นแล้ว</li><li>**การคํานวณการทำงาน:** เนื่องจากค่าลิขสิทธิ์เกินจํานวนเงินประกัน $0 มีการลงรายการบัญชีในหนังสือค้ําประกัน</li></ul><p>**หมายเหตุ:** ควรคํานวณและลงรายการบัญชีการค้ําประกันพร้อมเฉพาะกับธุรกรรมการหักลดและเงินคืนสําหรับรอบระยะเวลาสุดท้าย</p></li></ul> |
| ค้ําประกันขั้นต่ำ | ฟิลด์นี้จะใช้กับข้อตกลงของค่าลิขสิทธิ์เท่านั้น ป้อนยอดเงินขั้นต่ําของหนังสือค้ําประกันของค่าลิขสิทธิ์ในสกุลเงินที่กําหนดไว้ในหัวข้อข้อตกลง |

### <a name="settings-on-the-lines-tab"></a>การตั้งค่าบนแท็บรายการ

แท็บ **รายการ** บนแท็บด่วน **รายละเอียดการจัดการเงินคืน** ช่วยให้คุณระบุวิธีการคํานวณเกี่ยวกับรายการข้อตกลงที่เลือก รายการการคํานวณแต่ละรายการจะสร้างปริมาณหรือค่าขีดเส้นตรง และจํานวนเงินหรือสินค้าค่าตอบแทนที่เกี่ยวข้อง ฟิลด์ **พื้นฐาน** บน **ทั่วไป** จะระบุว่าแต่ละบรรทัดการคํานวณขึ้นอยู่กับปริมาณหรือค่า

คุณสามารถใช้ปุ่มบนแถบเครื่องมือเพื่อเพิ่มรายการการคํานวณลงในกริด หรือเพื่อลบ คุณสามารถมีรายการการคํานวณได้หลายรายการ อย่างไรก็ตาม ถ้ามีรายการการคํานวณหลายรายการ ปริมาณ "ถึง" และ "เริ่มต้น" หรือช่วงค่าต้องไม่ทับซ้อนกัน

ตารางต่อไปนี้อธิบายถึงฟิลด์ที่พร้อมใช้งานสำหรับสินค้าแต่ละการคํานวณ

| ฟิลด์ | คำอธิบาย |
|---|---|
| ปริมาณ/มูลค่าเริ่มต้น | ป้อนปริมาณหรือค่าขั้นต่ำที่จะใช้กับรายการการคํานวณ |
| ปริมาณ/มูลค่าสูงสุด | ป้อนปริมาณหรือค่าสูงสุดที่จะใช้กับรายการการคํานวณ |
| วิธีการจัดการเงินคืน | <p>ฟิลด์นี้จะพร้อมใช้งานเฉพาะกับข้อตกลงที่มีการตั้งค่าฟิลด์ **เอาท์พุทเงินคืน** บนส่วนหัวเป็น *ทางการเงิน* เท่านั้น เลือกวิธีการที่จะใช้ในการคำนวณเงินคืน:</p><ul><li>*คงที่* – ใช้ยอดราคาคงที่ของบรรทัด</li><li>*เปอร์เซ็นต์* – ใช้เปอร์เซ็นต์ของยอดการขาย</li><li>*อัตรา* – ใช้ยอดราคาคงที่ต่อใบสั่ง</li></ul><p>**ข้อสําคัญ:** เราขอแนะให้ใช้วิธีการเดียวกันนี้กับทุกบรรทัดการคํานวณบนแท็บ **รายการ** ถ้าต้องใช้วิธีการใหม่ ให้สร้างรายการข้อตกลงใหม่ โปรดอย่าลืมว่าคุณสามารถใช้ปุ่ม **คัดลอกรายการ** บนแท็บด่วน **การจัดการเงินคืน** เพื่อสร้างรายการข้อตกลงใหม่จากรายการข้อตกลงที่มีอยู่</p><p>**หมายเหตุ:** ถ้าตั้งค่าฟิลด์ **เอาท์พุทเงินคืน** เป็น *สินค้า* ฟิลด์นี้จะถูกตั้งค่าเป็น *คงที่* เสมอ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีระบุสินค้า ให้ดูที่ข้อความที่ตามมาในตารางนี้ |
| จำนวนการจัดการเงินคืน | ฟิลด์นี้จะพร้อมใช้งานเฉพาะกับข้อตกลงที่มีการตั้งค่า **เอาท์พุทเงินคืน** บนส่วนหัวเป็น *ทางการเงิน* เท่านั้น ป้อนจํานวนเงินที่ควรจะใช้ในการคํานวณเงินคืน ตามวิธีการที่คุณเลือกในฟิลด์ **วิธีการจัดการเงินคืน** |

ตามที่กล่าวถึงในตารางก่อนหน้านี้ ให้กับข้อตกลงที่มีการตั้งค่าฟิลด์ **เอาท์พุทเงินคืน** ในส่วนหัวเป็น *สินค้า* คุณต้องระบุสินค้าที่จะจัดเตรียมไว้ให้กับบรรทัดการคํานวณทุกบรรทัดบนแท็บ **รายการ** หากต้องการระบุสินค้า ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. บนแท็บ **รายการ** ให้สร้างบรรทัดการคํานวณที่ต้องใช้ถ้าไม่มีบรรทัดนั้นอยู่ และเลือกบรรทัดนั้น
1. ถ้ายังไม่ได้บันทึกข้อตกลงนับตั้งแต่คุณสร้างรายการการคํานวณ ให้เลือก **บันทึก** บนบานหน้าต่างการดำเนินการ
1. บนแท็บ **รายการ** เลือก **สินค้า**
1. บนหน้า **สินค้า** ให้ใช้ปุ่มต่าง ๆ ในบานหน้าต่างการดำเนินการเพื่อเพิ่มสินค้าลงในกริด หรือลบสินค้าออกตามต้องการ สำหรับแต่ละแถว กำหนดค่าฟิลด์ต่อไปนี้:

    - **หมายเลขสินค้า** – เลือกสินค้าที่จะจัดเตรียมให้
    - **(มิติอื่น)** – ถ้าคุณต้องใช้มิติเพิ่มเติมเพื่อกําหนดสินค้า (ตัวอย่างเช่น โครงแบบสินค้า ขนาด สี ลักษณะ ไซต์ หรือคลังสินค้า) ให้ระบุ เมื่อต้องการเพิ่มหรือลบมิติพร้อมใช้งาน ให้เลือก **แสดงมิติ** ในบานหน้าต่างการดำเนินการ
    - **ปริมาณ** - ป้อนปริมาณที่จะระบุหลังจากขีดจำกัดของรายการการคํานวณที่เลือก
    - **หน่วย** – เลือกหน่วยที่ค่า **ปริมาณ** ระบุไว้
    - **หลายรายการ** – ฟิลด์นี้จะทำงานพร้อมกับฟิลด์ **ปริมาณ** ตัวอย่างเช่น บนรายการสินค้า คุณตั้งค่าฟิลด์ **ปริมาณ** เป็น *2* และฟิลด์ **หลายฟิลด์** เป็น *100* จากนั้นถ้าคุณมีปริมาณใบสั่งขายรวมเท่ากับ 150 สินค้าสองรายการจะได้รับฟรี (สองชิ้นต่อ 100)

### <a name="settings-on-the-inventory-dimensions-tab"></a>การตั้งค่าบนแท็บมิติสินค้าคงคลัง

แท็บ **มิติสินค้าคงคลัง** บนแท็บด่วน **รายละเอียดการจัดการเงินคืน** แสดงค่ามิติที่พร้อมใช้งานทั้งหมดของผลิตภัณฑ์ที่ระบุไว้ให้กับรายการข้อตกลงที่เลือก โดยรวมมิติที่ไม่ได้แสดงอยู่บนแท็บด่วน **การจัดการเงินคืน** คุณสามารถแก้ไขค่าได้เฉพาะกับมิติที่ใช้กับผลิตภัณฑ์ที่เลือกเท่านั้น

คุณสามารถเพิ่มมิติเพิ่มเติมที่กริดบนแท็บด่วน **การจัดการเงินคืน** ได้โดยเลือก **มิติแสดงผล** ในบานหน้าต่างการดำเนินการ

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>วิธีการคํานวณรายการราคา

ทุกครั้งที่คุณตั้งค่ารายละเอียดบรรทัดข้อตกลงใดบรรทัดหนึ่งของคุณ ตามที่อธิบายไว้ในส่วนก่อนหน้านี้ คุณต้องเลือกวิธีการคํานวณของบรรทัดนั้น ส่วนนี้จะอธิบายถึงวิธีการคํานวณแต่ละวิธีและแสดงตัวอย่างวิธีการที่แต่ละวิธีการคํานวณเงินคืนรวมของใบสั่งและรายการข้อตกลง ในตัวอย่างเหล่านี้ ใบสั่งและบรรทัดข้อตกลงเหมือนกัน เฉพาะวิธีการคํานวณเท่านั้นที่แตกต่างกัน

### <a name="stepped-calculation-method"></a>วิธีการคำนวณแบบเพิ่มขึ้นตามขั้น

วิธีการคำนวณแบบเพิ่มขึ้นตามขั้นเป็นขั้นตอน โดยที่รายการข้อตกลงแต่ละรายการจะเพิ่มขึ้นในเงินคืนจนกว่าจะครบปริมาณหรือมูลค่าการขาย ขั้นตอนอาจขึ้นอยู่กับปริมาณหรือมูลค่าของสินค้าที่ขาย ทั้งนี้ขึ้นอยู่กับการตั้งค่าฟิลด์ **พื้นฐาน** บนแท็บ **ทั่วไป** ของแท็บด่วน **รายละเอียดการจัดการเงินคืน**

ตัวอย่างเช่น บรรทัดข้อตกลงมีการตั้งค่าเพื่อให้ฟิลด์ **วิธีการคํานวณ** ถูกตั้งค่าเป็น *เพิ่มขึ้นตามขั้น* และฟิลด์ **ข้อมูลพื้นฐาน** จะถูกตั้งค่าเป็น *ค่า* ซึ่งรวมถึงรายการคํานวณที่ให้เงินคืนดังต่อไปนี้:

- **บรรทัด A:** 10 เปอร์เซ็นต์ถึง $1,000
- **บรรทัด B:** 25 เปอร์เซ็นต์ถึง $2,500

หากมีการคํานวณมูลค่าของสินค้าที่ซื้อหรือขาย $2,000 เงินคืนที่ได้รับ $350 จะคํานวณในลักษณะต่อไปนี้

- **เงินคืน (A):** *ขีดจำกัด (A)* × *เปอร์เซ็นต์ (A)* = $1,000 × 10 เปอร์เซ็นต์ = $100
- **เงินคืน (B):** (*ค่าที่ขาย* – *ขีดจำกัด (A)*) × *เปอร์เซ็นต์ (B)* = ($2,000 – $1,000) × 25 เปอร์เซ็นต์ = $250
- **เงินคืนรวม:** *เงินคืน (A)* + *เงินคืน (B)* = $100 + $250 = $350

ถ้าฟิลด์ **ข้อมูลพื้นฐาน** มีการตั้งค่าเป็น *ปริมาณ* แทน *ค่า* วิธีการคํานวณที่จัดขั้นตอนจะใช้งานในลักษณะที่คล้ายกัน ขั้นตอนแรกจะใช้กับปริมาณที่ระบุจนกว่าจะถึงขั้นตอนที่สอง ขั้นตอนที่สองจะใช้กับปริมาณทั้งหมดจากขั้นตอนแรก จนกว่าจะถึงขั้นตอนที่สาม จากนั้นกระบวนการนี้จะยังคงผ่านขั้นตอนต่อมาทั้งหมด

### <a name="cumulative-calculation-method"></a>วิธีการคำนวณสะสม

วิธีการคํานวณสะสมจะใช้รายการคํานวณเพียงรายการเดียวในการคํานวณเงินคืน ถ้าบรรทัดการคํานวณหลายบรรทัดมีอยู่บรรทัดข้อตกลง ค่าสูงสุดหรือบรรทัดการคํานวณปริมาณสูงสุดที่ครบแล้วจะใช้กับปริมาณหรือมูลค่าทั้งหมด เช่นเดียวกับวิธีการคํานวณอื่นๆ วิธีการสะสมจะใช้การตั้งค่าฟิลด์ **ข้อมูลพื้นฐาน** บนแท็บ **ทั่วไป** ของแท็บด่วน **รายละเอียดการจัดการเงินคืน** เพื่อระบุว่าปริมาณการขายหรือมูลค่าการขายจะใช้เพื่อคํานวณเงินคืนหรือไม่

ตัวอย่างเช่น บรรทัดข้อตกลงมีการตั้งค่าเพื่อให้ฟิลด์ **วิธีการคํานวณ** ถูกตั้งค่าเป็น *สะสม* และฟิลด์ **ข้อมูลพื้นฐาน** จะถูกตั้งค่าเป็น *ค่า* ซึ่งรวมถึงรายการคํานวณที่ให้เงินคืนดังต่อไปนี้:

- **บรรทัด A:** 10 เปอร์เซ็นต์ถึง $1,000
- **บรรทัด B:** 25 เปอร์เซ็นต์ถึง $2,500

หากมีการคํานวณมูลค่าของสินค้าที่ซื้อหรือขาย $2,000 การคำนวณจะใช้เฉพาะรายการ B เงินคืนที่ได้รับ $500 จะคํานวณในลักษณะต่อไปนี้

- **เงินคืนรวม:** *ค่าที่ขาย* × *เงินคืน (B)* = $2,000 × 25 เปอร์เซ็นต์ = $500

### <a name="rolling-calculation-method"></a>วิธีการคำนวณย้อนหลัง

วิธีการคํานวณย้อนหลังจะคํานวณรายการคํานวณที่เป็นไปได้ทั้งหมด ถ้ามีบรรทัดการคํานวณมากกว่าหนึ่งบรรทัด และบรรทัดใดบรรทัดหนึ่งมากกว่าหนึ่งบรรทัด ก็จะใช้บรรทัดการคํานวณทั้งหมดที่มาถึง แต่ขีดจำกัดสูงสุดจะใช้กับแต่ละเปอร์เซ็นต์ เช่นเดียวกับวิธีการคํานวณอื่นๆ วิธีการย้อนหลังจะใช้การตั้งค่าฟิลด์ **ข้อมูลพื้นฐาน** บนแท็บ **ทั่วไป** ของแท็บด่วน **รายละเอียดการจัดการเงินคืน** เพื่อระบุว่าปริมาณการขายหรือมูลค่าการขายจะใช้เพื่อคํานวณเงินคืนหรือไม่

ตัวอย่างเช่น บรรทัดข้อตกลงมีการตั้งค่าเพื่อให้ฟิลด์ **วิธีการคํานวณ** ถูกตั้งค่าเป็น *ย้อนหลัง* และฟิลด์ **ข้อมูลพื้นฐาน** จะถูกตั้งค่าเป็น *ค่า* ซึ่งรวมถึงรายการคํานวณที่ให้เงินคืนดังต่อไปนี้:

- **บรรทัด A:** 10 เปอร์เซ็นต์ถึง $1,000
- **บรรทัด B:** 25 เปอร์เซ็นต์ถึง $2,500

หากมีการคํานวณมูลค่าของสินค้าที่ซื้อหรือขาย $2,000 เงินคืนที่ได้รับ $600 จะคํานวณในลักษณะต่อไปนี้

- **เงินคืน (A):** *ขีดจำกัด (A)* × *เปอร์เซ็นต์ (A)* = $1,000 × 10 เปอร์เซ็นต์ = $100
- **เงินคืน (B):** *มูลค่าที่ขาย* × *เปอร์เซ็นต์ (B)* = $2,000 × 25 เปอร์เซ็นต์ = $500
- **เงินคืนรวม:** *เงินคืน (A)* + *เงินคืน (B)* = $100 + $500 = $600

### <a name="total-calculation-method"></a>วิธีการคำนวณรวม

วิธีการคํานวณรวมจะใช้รายการคํานวณทั้งหมดในการคํานวณเงินคืน การใช้ปริมาณรวมเพื่อคํานวณเงินคืนต่อรายการคํานวณแต่ละรายการที่มาถึง และรายการคํานวณแต่ละรายการจะใช้เปอร์เซ็นต์ของเงินคืนกับยอดเงินทั้งหมด เช่นเดียวกับวิธีการคํานวณอื่นๆ วิธีการรวมจะใช้การตั้งค่าฟิลด์ **ข้อมูลพื้นฐาน** บนแท็บ **ทั่วไป** ของแท็บด่วน **รายละเอียดการจัดการเงินคืน** เพื่อระบุว่าปริมาณการขายหรือมูลค่าการขายจะใช้เพื่อคํานวณเงินคืนหรือไม่

ตัวอย่างเช่น บรรทัดข้อตกลงมีการตั้งค่าเพื่อให้ฟิลด์ **วิธีการคํานวณ** ถูกตั้งค่าเป็น *รวม* และฟิลด์ **ข้อมูลพื้นฐาน** จะถูกตั้งค่าเป็น *ค่า* ซึ่งรวมถึงรายการคํานวณที่ให้เงินคืนดังต่อไปนี้:

- **บรรทัด A:** 10 เปอร์เซ็นต์ถึง $1,000
- **บรรทัด B:** 25 เปอร์เซ็นต์ถึง $2,500

หากมีการคํานวณมูลค่าของสินค้าที่ซื้อหรือขาย $2,000 เงินคืนที่ได้รับ $700 จะคํานวณในลักษณะต่อไปนี้

- **เงินคืน (A):** *มูลค่าที่ขาย* × *เปอร์เซ็นต์ (A)* = $2,000 × 10 เปอร์เซ็นต์ = $200
- **เงินคืน (B):** *มูลค่าที่ขาย* × *เปอร์เซ็นต์ (B)* = $2,000 × 25 เปอร์เซ็นต์ = $500
- **เงินคืนรวม:** *เงินคืน (A)* + *เงินคืน (B)* = $200 + $500 = $700
