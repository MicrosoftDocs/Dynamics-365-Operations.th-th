---
title: ขยาย Talent ด้วย Power Apps และ Power Automate
description: บทความนี้อธิบายถึงตัวอย่างบางรายการของสถานการณ์การเพิ่มความสามารถของ Microsoft Dynamics 365 Talent - Attract ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029922"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>ขยาย Talent ด้วย Power Apps และ Power Automate

บทความนี้อธิบายถึงตัวอย่างบางรายการของสถานการณ์การเพิ่มความสามารถของ Microsoft Dynamics 365 Talent: Attract ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate คุณสามารถนำเข้าโซลูชันแพคเกจที่เชื่อมโยงกับแต่ละตัวอย่างไปยังสภาพแวดล้อม Power Apps ของคุณ จากนั้นคุณสามารถใช้แพคเกจเป็นคำแนะนำหรือเป็นจุดเริ่มต้นเพื่อนำสถานการณ์ที่สามารถใช้ได้กับองค์กรของคุณไปใช้

> [!IMPORTANT]
> ถ้าคุณต้องการใช้เท็มเพลตและแอปที่อธิบายไว้ในบทความนี้ "ตามที่เป็น" ให้แน่ใจว่าได้ทดสอบแล้วเพื่อให้แน่ใจว่าจะครอบคลุมสถานการณ์จำลองทั้งหมดที่เกี่ยวข้องกับการนำไปใช้ของคุณโดยเฉพาะ


## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

- เมื่อต้องการนำเข้าแพคเกจ ผู้ใช้ต้องมีสิทธิ์ **ผู้สร้างสภาพแวดล้อม**
- เมื่อต้องการส่งออกหรือนำเข้าแอป ผู้ใช้ต้องมีใบอนุญาตใช้ Power Apps Plan 2 หรือใบอนุญาตในการทดลองใช้ Power Apps Plan 2

## <a name="power-automate--form-connect"></a>Power Automate – การเชื่อมต่อฟอร์ม

แม่แบบ **Power Automate – การเชื่อมต่อฟอร์ม** สามารถนำมาใช้เพื่ออ่านข้อมูลจาก Microsoft Forms และจัดเก็บไว้ในเอนทิตี Common Data Service ได้

เท็มเพลตนี้สามารถขยายได้เพื่อให้สามารถใช้สำหรับสถานการณ์จำลองอื่น ๆ ยกตัวอย่างเช่น

- รวบรวมการประเมินผู้สมัคร
- รวบรวมผลลัพธ์จากแบบสอบถามของหลักสูตร
- คอมไพล์ไลบรารีของคำถามสัมภาษณ์สำหรับผู้ดูแลฝ่ายทรัพยากรบุคคล (HR)
- เก็บรวบรวมการประเมินของผู้สมัครของกระบวนการสัมภาษณ์

ใน Microsoft Dynamics 365: Attract คุณสามารถใช้ฟอร์มในพอร์ทัลของผู้สมัคร ที่ซึ่งผู้สมัครสามารถกรอกข้อมูลโดยใส่รายละเอียดได้ นอกจากนี้ คุณยังสามารถฝังฟอร์มเป็นกิจกรรมในเท็มเพลตงานได้อีกด้วย

เมื่อผู้สมัครส่งฟอร์ม Microsoft Power Automate จะเก็บรวบรวมการส่งฟอร์ม อ่านข้อมูล และเก็บไว้ในเอนทิตี Common Data Service

เมื่อต้องการดาวน์โหลดแม่แบบ **Power Automate – การเชื่อมต่อฟอร์ม** และโครงสร้างการกำหนดเอนทิตีด้วยตนเอง ไปที่ [Power Automate – การเชื่อมต่อฟอร์ม](https://go.microsoft.com/fwlink/?linkid=2081988) บนศูนย์ดาวน์โหลด Microsoft

## <a name="power-automate--sharepoint-integration"></a>Power Automate – การรวม SharePoint

คุณสามารถใช้แม่แบบ **Power Automate – การรวม SharePoint** เพื่ออ่านข้อมูลจากรายการ Microsoft SharePoint เปรียบเทียบรายการที่มีค่าฟิลด์สำหรับเอนทิตี Common Data Service ใด ๆ และส่งผลลัพธ์ของการเปรียบเทียบเป็นอีเมลการแจ้งเตือนได้ 

องค์กรอาจมีชุดของทักษะที่ต้องใช้โดยทันที คุณสามารถจัดเก็บทักษะเหล่านี้ใน SharePoint เป็นรายการ SharePoint เมื่อผู้สมัครสมัครสำหรับงานใด ๆ ที่มีแสดงรายการชุดของทักษะที่จำเป็น ถ้ามีการจับคู่ที่มีนัยสำคัญระหว่างทักษะของผู้สมัครและทักษะที่เก็บไว้ใน SharePoint จะมีการส่งอีเมลการแจ้งเตือน นี่จะช่วยในการกรอกข้อมูลตำแหน่งที่จำเป็นต้องจัดหาโดยเร่งด่วน เนื่องจากการแจ้งเตือนจะช่วยให้ผู้สรรหาสามารถว่าจ้างผู้สมัครได้ทั่วทั้งองค์กร

คุณสามารถขยายเท็มเพลตนี้เพื่อให้สามารถใช้สำหรับสถานการณ์จำลองใด ๆ ที่เกี่ยวข้องกับการรวม SharePoint ได้

เมื่อต้องการดาวน์โหลดแม่แบบ **Power Automate – การรวม SharePoint** ไปที่ [Power Automate – กาารรวม SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) บนศูนย์ดาวน์โหลด Microsoft

## <a name="referral-app"></a>แอปการอ้างอิง

คุณสามารถใช้แอปการอ้างอิงเพื่อเพิ่มผู้สมัครในกลุ่มผู้มีความสามารถพิเศษที่ใช้ร่วมกัน การอ้างอิงสามารถป้อน **Firstname** **Lastname** **อีเมล** และ **URL ของ LinkedIn** เมื่อส่งผู้สมัคร ข้อมูลเมตาของแหล่งที่มาของผู้สมัครจะถูกเติมด้วยข้อมูลของบุคคลอ้างอิง

คุณสามารถฝังแอปนี้ในระบบบริการตนเองของพนักงานสำหรับการส่งการอ้างอิง หรือคุณสามารถใช้เป็นไฮเปอร์ลิงค์ในพอร์ทัลองค์กรและรันเป็นแอปที่ทำงานแยกต่างหาก

เมื่อต้องการดาวน์โหลด **แอปการอ้างอิง** ไปที่ [โซลูชันความสามารถในการเพิ่มฟังก์ชัน Dynamics 365 Talent : แอปการอ้างอิง](https://www.microsoft.com/download/details.aspx?id=58497) บนศูนย์การดาวน์โหลดของ Microsoft คุณสามารถนำเข้าแอปนี้และเลือกกำหนดเพื่อเพิ่มฟังก์ชันเพิ่มเติมได้

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[ย้ายแอประหว่างผู้เช่าและสภาพแวดล้อม](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
