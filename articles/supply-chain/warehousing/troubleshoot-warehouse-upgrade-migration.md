---
title: แก้ไขการอัปเกรดและการโยกย้ายไปที่การจัดการคลังสินค้าขั้นสูง
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณอัปเกรดและการโยกย้ายไปที่การจัดการคลังสินค้าขั้นสูง
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993911"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>แก้ไขการอัปเกรดและการโยกย้ายไปที่การจัดการคลังสินค้าขั้นสูง

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณอัปเกรดและการโยกย้ายไปที่การจัดการคลังสินค้าขั้นสูง

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "java.security.cert.certPathValidatorException: ไม่พบจุดยึดของความเชื่อถือสำหรับเส้นทางใบรับรอง"

### <a name="issue-description"></a>คำอธิบายปัญหา

คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดในแอปคลังสินค้าเนื่องจากใบรับรองที่มีการลงชื่อด้วยตนเองไม่ได้รับความไว้วางใจในสภาพแวดล้อม Android 8+ ในสถานที่

### <a name="issue-resolution"></a>การแก้ไขปัญหา

ใช้หน่วยงานรับรองภายนอก (สาธารณะ) (CA) การแก้ไขสำหรับปัญหานี้จะพร้อมใช้งานในรุ่น 1.9.0.0 ของแอปคลังสินค้า สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตัดสินค้าจากคลังและวิธีการแก้ไข ให้ดูที่ [แก้ไขปัญหาเกี่ยวกับการเชื่อมต่อของแอปคลังสินค้า](troubleshoot-warehouse-app-connection.md)

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>กระบวนการที่ได้รับการอนุมัติสำหรับการเคลื่อนย้ายจากคลังสินค้าขั้นพื้นฐานไปยังคลังสินค้าขั้นสูงมีอะไรบ้าง

### <a name="issue-description"></a>คำอธิบายปัญหา

ขณะนี้คุณกำลังทำงานอยู่ภายใต้การบริหารสต็อก/สินค้าคงคลังและการใช้ฟังก์ชันการทำงานพื้นฐานของสินค้าคงคลัง และคุณต้องการย้ายไปยังคลังสินค้าขั้นสูงเพื่อใช้ประโยชน์จากอุปกรณ์เคลื่อนที่ เวฟ และงาน อย่างไรก็ตาม คุณกำลังประสบปัญหาเมื่อคุณพยายามทำการย้าย ตัวอย่างเช่น คุณไม่สามารถเปลี่ยนผลิตภัณฑ์ของคุณเพื่อให้ใช้มิติการจัดเก็บ (ไซต์ คลังสินค้า และสถานที่เก็บ) เนื่องจากผลิตภัณฑ์มีธุรกรรมอยู่ ดังนั้น คุณต้องเรียนรู้กระบวนการที่ได้รับการอนุมัติสำหรับการเคลื่อนย้ายจากคลังสินค้าขั้นพื้นฐานไปยังคลังสินค้าขั้นสูง

### <a name="issue-resolution"></a>การแก้ไขปัญหา

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการสำหรับการย้ายจากคลังสินค้าพื้นฐานไปยังคลังสินค้าขั้นสูง ให้ดูที่การลงรายการบัญชีและเอกสารต่อไปนี้ของบล็อก:

- [เปิดใช้งานสำหรับกระบวนการบริหารคลังสินค้าสำหรับสินค้าและคลังสินค้าที่มี](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [การโยกย้ายของ Microsoft Dynamics AX WMS ไปยังคลังสินค้า R3 ใหม่และฟังก์ชันการขนส่ง](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [การย้ายสินค้า WMSI/WMS2](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [อัพเกรดการจัดการคลังสินค้าจาก Microsoft Dynamics AX 2012 ไปยัง Supply Chain Management](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]