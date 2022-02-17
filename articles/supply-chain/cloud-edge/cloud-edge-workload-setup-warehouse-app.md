---
title: ตั้งค่าคอนฟิกแอป Warehouse Management บนมือถือสำหรับสเกลยูนิตในระบบคลาวด์และแบบปลายทาง
description: หัวข้อนี้จะอธิบายวิธีตั้งค่าแอป Warehouse Management บนมือถือสำหรับคลังสินค้าซึ่งให้บริการโดยสเกลยูนิตในระบบคลาวด์และแบบปลายทาง
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 1fa00b40db2f6246029876964dca9d3229567848
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071664"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>ตั้งค่าคอนฟิกแอป Warehouse Management บนมือถือสำหรับสเกลยูนิตในระบบคลาวด์และแบบปลายทาง

[!include [banner](../includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีตั้งค่าแอป Warehouse Management บนมือถือเพื่อให้สามารถใช้กับคลังสินค้าซึ่งให้บริการโดยสเกลยูนิตในระบบคลาวด์และแบบปลายทาง

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มตั้งค่าอุปกรณ์เคลื่อนที่เพื่อเชื่อมต่อกับสเกลยูนิตในระบบคลาวด์และแบบปลายทาง ให้ยืนยันว่าอุปกรณ์สามารถเชื่อมต่อกับฮับองค์กรได้ สำหรับคำแนะนำ ให้ดูที่ [ติดตั้งและเชื่อมต่อแอป Warehouse Management บนมือถือ](../warehousing/install-configure-warehouse-management-app.md)

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>การตั้งค่าเพิ่มเติมเมื่อคุณเรียกใช้แอป Warehouse Management บนมือถือกับสเกลยูนิต

ในฐานะส่วนหนึ่งของ [กระบวนการปรับใช้งานสำหรับปริมาณงานสเกลยูนิตของคลังสินค้า](cloud-edge-landing-page.md#scale-unit-manager-portal) ข้อมูลส่วนใหญ่ที่ต้องใช้ในการเชื่อมต่ออุปกรณ์ที่มีแอป Warehouse Management บนมือถือจะได้รับการซิงค์โดยอัตโนมัติจากฮับองค์กรไปยังสเกลยูนิต อย่างไรก็ตาม คุณต้องป้อนข้อมูลในหน้า **แอปพลิเคชัน Azure Active Directory** (**การดูแลระบบ \> การตั้งค่า \> แอปพลิเคชัน Azure Active Directory**) ในการปรับใช้สเกลยูนิต นอกจากนี้ คุณอาจต้องอัปเดตค่า **บริษัท** เริ่มต้นสำหรับรหัสผู้ใช้หรือสร้างผู้ใช้ใหม่ ผู้ใช้ที่เชื่อมโยงกับบริษัทที่ไม่มีอยู่ในการปรับใช้สเกลยูนิตจะไม่สามารถล็อกอินได้ เมื่อแอป Warehouse Management บนมือถือเชื่อมต่อกับสเกลยูนิตนั้น

> [!NOTE]
> เนื่องจากข้อมูลในหน้า **แอปพลิเคชัน Azure Active Directory** ไม่ได้ซิงค์กัน คุณจึงต้องดูแลรักษาข้อมูลนี้ด้วยตนเองหากคุณต้องการย้ายปริมาณงานของคลังสินค้าไปยังสเกลยูนิตอื่น

โปรดอย่าลืมว่าในฐานะเป็นส่วนหนึ่งของการตั้งค่าแอป Warehouse Management บนมือถือแต่ละรายการ URL ทรัพยากร Azure Active Directory ที่ระบุต้องเป็นสำหรับสเกลยูนิตแทนฮับองค์กร
