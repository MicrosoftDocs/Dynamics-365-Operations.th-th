---
title: เก็บถาวรใบแจ้งหนี้ของลูกค้าที่พิมพ์ออกมาด้วยหมายเลขแฮช
description: บทความนี้อธิบายวิธีการเปิดใช้งานการเก็บถาวรเพื่อจัดเก็บใบแจ้งหนี้ของลูกค้าที่พิมพ์ออกมาพร้อมหมายเลขแฮช
author: mrolecki
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.custom: 539093
ms.search.form: ''
ms.openlocfilehash: 4c9bd7ead1615a4e6b0e8e672e858312ba518b56
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291683"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>เก็บถาวรใบแจ้งหนี้ของลูกค้าที่พิมพ์ออกมาด้วยหมายเลขแฮช

[!include [banner](../includes/banner.md)]

ในบางประเทศ มีข้อกําหนดทางกฎหมายในการจัดเก็บหมายเลขแฮชที่คํานวณได้ในระบบร่วมกับการพิมพ์เอกสารบางฉบับ สามารถใช้หมายเลขแฮชเพื่อรายงานต่อหน่วยงานจัดเก็บภาษีและในระหว่างการตรวจสอบ

บทความนี้อธิบายวิธีการกำหนดค่าการเก็บถาวรเพื่อจัดเก็บใบแจ้งหนี้ของลูกค้าที่พิมพ์ออกมาพร้อมหมายเลขแฮช

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

- ในพื้นที่ **จัดการลักษณะ** ให้เปิดคุณสมบัติ **ใบกำกับสินค้าที่พิมพ์พร้อมด้วยหมายเลขแฮช** สำหรับข้อมูลเพิ่มเติม ดูที่ [ภาพรวมการจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)
- ต้องตั้งค่าคอนฟิกรูปแบบที่สามารถพิมพ์ได้ของเอกสารที่กําหนดใน **การจัดการการพิมพ์**

ฟังก์ชันนี้สามารถใช้ได้กับเอกสารต่อไปนี้

**บัญชีลูกหนี้**
- ใบแจ้งหนี้ของลูกค้า
- ใบลดหนี้ของลูกค้า
- ใบแจ้งหนี้ข้อความอิสระ
- ใบลดหนี้ข้อความอิสระ

**การจัดการและการบัญชีโครงการ**
- ใบแจ้งหนี้ของโครงการ
- ใบลดหนี้ของโครงการ

## <a name="configure-customer-master-data"></a>กำหนดค่าข้อมูลหลักของลูกค้า
ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกข้อมูลลูกค้าและเปิดความสามารถในการบันทึกใบแจ้งหนี้ที่พิมพ์เป็นเอกสารแนบโดยอัตโนมัติ

1. ไปที่ **บัญชีลูกหนี้** > **ลูกค้าทั้งหมด** 
2. เลือกลูกค้า และบน FastTab **ใบแจ้งหนี้และการจัดส่ง** ในส่วน **E-INVOCE** ในฟิลด์ **เอกสารแนบ eInvoice** ให้เลือก **ใช่**

## <a name="print-invoices"></a>พิมพ์ใบแจ้งหนี้
คุณสามารถลงรายการบัญชีและพิมพ์ข้อความอิสระ ลูกค้า และใบแจ้งหนี้โครงการ หรือใบลดหนี้ใดๆ ของลูกค้าที่กำหนดค่าคอนฟิกในกระบวนการก่อนหน้า

เปิดหน้า **เอกสารแนบ** ของใบแจ้งหนี้ที่พิมพ์ออกมา บน FastTab **เอกสารแนบ** ในกลุ่มฟิลด์ **รายละเอียดเพิ่มเติม** ในฟิลด์ **หมายเลขเอกสารแฮช** ให้ค้นหาหมายเลขแฮชที่จัดเก็บซึ่งคํานวณไว้สำหรับใบแจ้งหนี้ที่พิมพ์ออกมา

![หมายเลขแฮชของเอกสารแนบ](media/attach-hash-num.jpg)

