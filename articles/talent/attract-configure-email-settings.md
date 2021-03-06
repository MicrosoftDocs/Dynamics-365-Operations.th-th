---
title: ตั้งค่าคอนฟิกการตั้งค่าอีเมลใน Attract
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกการตั้งค่าสำหรับอีเมลที่ส่งโดย Microsoft Dynamics 365 Talent - Attract
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: e641e3f0d1873d91be1a1dc9bc22eb734a2b21d5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462679"
---
# <a name="configure-email-settings-in-attract"></a>ตั้งค่าคอนฟิกการตั้งค่าอีเมลใน Attract

[!include [banner](includes/banner.md)]

แบรนด์ของคุณสร้างความไว้วางใจและช่วยคุณในการสร้างความสัมพันธ์กับผู้สมัคร ก่อนที่พวกเขาจะสมัครตำแหน่งของคุณ การรับรู้แบรนด์ในเชิงบวกดึงดูด talent สูงสุด และเพิ่มความภักดีของพนักงานที่มีอยู่ Microsoft Dynamics 365 Talent: Attract: ให้คุณตั้งค่าคอนฟิกอีเมล เพื่อให้สะท้อนถึงแบรนด์ของบริษัทของคุณ ดังนั้น คุณจึงสามารถให้ประสบการณ์ที่สอดคล้องกับผู้สมัครงานได้ เนื่องจากทำการดำเนินการผ่านกระบวนการแอพลิเคชัน

Attract อนุญาตให้คุณทำการดำเนินการเหล่านี้ได้:

- ตั้งค่าคอนฟิกการตั้งค่าอีเมล เพื่อให้มีการใช้บัญชีบริการอีเมลของ Microsoft Exchange ของบริษัทของคุณ ในลักษณะนี้ ผู้สมัครทราบว่าอีเมลมาจากบริษัทของคุณ ตัวอย่างเช่น คุณสามารถตั้งค่าคอนฟิกการตั้งค่าของคุณ เพื่อให้ผู้สมัครได้รับอีเมลจาก `recruiting@contoso.com` แทน `contoso@microsoft.com`
- สร้างการสร้างแบรนด์ที่สอดคล้องสำหรับการสื่อสารทางอีเมลของคุณทั้งหมด โดยการตั้งค่าส่วนหัวและส่วนท้ายส่วนกลางสำหรับเท็มเพลตอีเมล 

> [!NOTE]
> เมื่อต้องการตั้งค่าคอนฟิก Attract เพื่อให้ใช้บัญชีบริการอีเมลของบริษัทของคุณในการส่งอีเมล คุณต้องมี add-on ของการจ้างงานที่ครอบคลุม

## <a name="connect-an-email-service-account"></a>เชื่อมต่อบัญชีบริการอีเมล

โดยการเชื่อมต่อบัญชีบริการอีเมลของบริษัทของคุณ คุณสามารถสร้างประสบการณ์อีเมลที่มีแบรนด์สำหรับผู้สมัครงานของคุณ ถ้าคุณไม่ได้เชื่อมต่อบัญชีบริษัทของคุณ Attract จะใช้บัญชีบริการอีเมลที่มีแบรนด์ของ Microsoft เริ่มต้น

1. เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์ในมุมขวาบน) และจากนั้น เลือก **ศูนย์การจัดการ**
2. บนแท็บ **การตั้งค่าอีเมล** ภายใต้ **บัญชีบริการอีเมล** ให้เลือก **เชื่อมต่อบัญชีบริษัท**

    ![การเชื่อมต่อบัญชีบริการอีเมลของบริษัทของคุณใน Attract](./media/attract-admin-email-service-accounts.png)

    สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างบัญชีอีเมลที่ใช้ร่วมกัน โปรดดู [กล่องจดหมายที่ใช้ร่วมกันใน Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes)

3. ในหน้าต่างการลงชื่อเข้าใช้ Microsoft ให้เข้าสู่ระบบโดยใช้ข้อมูลประจำตัวขององค์กรของคุณ
4. ถ้าคุณยังไม่ได้ตั้งค่าบัญชีบริการอีเมล หรือถ้าคุณต้องการเพิ่มบัญชีใหม่ ให้เลือก **เพิ่มบัญชีบริการใหม่** แล้วป้อนข้อมูลอีเมลของคุณ ถ้าคุณได้ตั้งค่าบัญชีบริการอีเมลที่คุณต้องการใช้แล้ว ให้เลือกบัญชีนั้น

เมื่อมีการตั้งค่าคอนฟิกบัญชีบริการอีเมลของคุณเสร็จเรียบร้อยแล้ว คุณจะเห็นการแสดงรายการภายใต้ **บัญชีบริการอีเมล**

## <a name="disconnect-an-email-service-account"></a>ยกเลิกการเชื่อมต่อบัญชีบริการอีเมล

ถ้าคุณต้องการหยุดใช้โดเมนของบริษัทของคุณในการสื่อสารทางอีเมลผ่าน Attract คุณสามารถยกเลิกการเชื่อมต่อบัญชีบริการอีเมลได้

1. เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์ในมุมขวาบน) และจากนั้น เลือก **ศูนย์การจัดการ**
2. บนแท็บ **การตั้งค่าอีเมล** ภายใต้ **บัญชีบริการอีเมล** เลือกปุ่ม **เพิ่มเติม** (จุดแนวตั้งสามจุด) ถัดจากบัญชีบริการอีเมลที่คุณต้องการยกเลิกการเชื่อมต่อ
3. เลือก **ยกเลิกการเชื่อมต่อบัญชีอีเมล**

    ![การยกเลิกการเชื่อมต่อบัญชีบริการอีเมลของบริษัทของคุณ](./media/attract-admin-disconnect-email-account.png)

4. เมื่อคุณได้รับพร้อมท์ให้ยืนยันการดำเนินงาน ให้เลือก **ยกเลิกการเชื่อมต่อ**

    ![การยืนยันการยกเลิกการเชื่อมต่อของบัญชีบริการอีเมลของบริษัทของคุณ](./media/attract-admin-email-confirm-disconnect.png)

ถ้าคุณไม่ได้เชื่อมต่อบัญชีบริการอีเมลอื่น อีเมลที่ถูกส่งจาก Attract จะใช้บัญชีบริการอีเมลที่มีแบรนด์ของ Microsoft เริ่มต้น

## <a name="configure-email-template-settings"></a>ตั้งค่าคอนฟิกการตั้งค่าเท็มเพลตอีเมล

คุณสามารถอัพโหลดรูปภาพโลโก้ของบริษัทของคุณและข้อมูลอื่นๆ เป็นส่วนหัวที่มีแบรนด์สำหรับอีเมลของคุณได้ นอกจากนี้ คุณยังสามารถให้ลิงค์ไปยังนโยบายความเป็นส่วนตัวและข้อกำหนดการใช้งานของคุณในส่วนท้ายอีเมล

> [!NOTE]
> คุณต้องปฏิบัติตามกฎหมายที่เกี่ยวข้องของประเทศหรือภูมิภาคของคุณ และรวมทั้งประเทศหรือภูมิภาคที่ควบคุมดูแลผู้รับอีเมล กฎหมายเหล่านี้รวมถึงกฎระเบียบการป้องกันสแปม

1. เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์ในมุมขวาบน) และจากนั้น เลือก **ศูนย์การจัดการ**
2. บนแท็บ **การตั้งค่าอีเมล** ภายใต้ **การตั้งค่าเท็มเพลตอีเมล** ให้ลากรูปภาพที่คุณต้องการใช้เป็นส่วนหัวของอีเมลของคุณในกล่องรูปภาพ หรือคลิกในกล่องรูปภาพเพื่อเรียกดูไฟล์ เมื่อต้องการเปลี่ยนรูปภาพที่มีอยู่ อันดับแรกคุณต้องเลือก **ลบ** ที่อยู่ถัดไป รูปภาพต้องเป็นไฟล์ JPEG JPG PNG หรือ SVG ขนาดที่แนะนำสำหรับรูปภาพคือ ความกว้างระหว่าง 25 และ 800 พิกเซล และความสูงระหว่าง 25 และ 150 พิกเซล ขนาดไฟล์สูงสุดสำหรับส่วนหัวคือ1เมกะไบต์ (MB)

    ![การเพิ่มรูปภาพสำหรับส่วนหัวของอีเมลของบริษัทของคุณ](./media/attract-admin-email-header.png)

3. ภายใต้ **นโยบายความเป็นส่วนตัวของคุณสำหรับการสื่อสาร** ให้ระบุลิงค์ไปยังนโยบายความเป็นส่วนตัวของบริษัทของคุณ ภายใต้ **ข้อกำหนดและเงื่อนไขของคุณสำหรับการสื่อสาร** ให้ระบุลิงค์ไปยังข้อตกลงการใช้งานของบริษัทของคุณ

    ![การเพิ่มลิงค์ไปยังนโยบายความเป็นส่วนตัวและข้อกำหนดการใช้งานของบริษัทของคุณสำหรับส่วนท้ายของอีเมล](./media/attract-admin-email-footer.png)

4. เลือก **บันทึก** เพื่อบันทึกการตั้งค่าเท็มเพลตอีเมลของคุณ


[!INCLUDE[footer-include](../includes/footer-banner.md)]