---
title: เปิดใช้งานการตั้งค่าชนิดอัตราแลกเปลี่ยนของสกุลเงินภาษีหัก ณ ที่จ่ายสากลและชนิดวันที่
description: บทความนี้จะอธิบายวิธีการเปิดใช้งานการตั้งค่าสากลของชนิดอัตราแลกเปลี่ยนสกุลเงินของภาษีหัก ณ ที่จ่ายและชนิดวันที่
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9db9cf41381b8b4de7dffe1c755a7df805a003ea
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573236"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>เปิดใช้งานการตั้งค่าชนิดอัตราแลกเปลี่ยนของสกุลเงินภาษีหัก ณ ที่จ่ายสากลและชนิดวันที่

[!include[banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการเปิดใช้งานการตั้งค่าสากลของชนิดอัตราแลกเปลี่ยนสกุลเงินของภาษีหัก ณ ที่จ่ายและชนิดวันที่ ขณะนี้คุณสามารถเลือกชนิดอัตราแลกเปลี่ยนที่จัดสรรไว้และชนิดวันที่ในการคํานวณอัตราแลกเปลี่ยนของสกุลเงินภาษีหัก ณ ที่จ่าย การเลือกเหล่านี้จะระบุอัตราแลกเปลี่ยนสกุลเงินต่างประเทศที่ใช้ในการคํานวณจํานวนเงินภาษีหัก ณ ที่จ่ายในสกุลเงินภาษีหัก ณ ที่จ่ายในธุรกรรมการจ่าย

ฟังก์ชันนี้มีอยู่ใน Microsoft Dynamics 365 Finance รุ่น 10.0.29 และรุ่นที่ใหม่กว่า

1. ไปที่ **ภาษี** \> **การตั้งค่า** \> **พารามิเตอร์** \> **พารามิเตอร์บัญชีแยกประเภททั่วไป**
2. บนแท็บ **ภาษีหัก ณ ที่จ่าย** ให้ตั้งค่าตัวเลือก **เปิดใช้งานสกุลเงินภาษีหัก ณ ที่จ่ายขั้นสูง** เป็น **ใช่**
3. ในฟิลด์ **ชนิดอัตราแลกเปลี่ยน** ให้เลือกชนิดอัตราแลกเปลี่ยนของสกุลเงินภาษีหัก ณ ที่จ่าย
4. ในฟิลด์ชนิด **วันที่คํานวณ** ให้เลือกชนิดวันที่ในการคํานวณที่เป็นตัวระบุอัตราแลกเปลี่ยนสกุลเงินของภาษีหัก ณ ที่จ่าย ดังนี้

    - **วันที่การชำระเงิน** – ระบุอัตราแลกเปลี่ยนตามวันที่ลงรายการบัญชีของสมุดรายวันการชำระเงิน
    - **วันที่ใบแจ้งหนี้** – ระบุอัตราแลกเปลี่ยนตามวันที่ใบแจ้งหนี้ของสมุดรายวันใบแจ้งหนี้ ถ้าวันที่ใบแจ้งหนี้ของใบสำคัญว่างเปล่า จะมีการใช้วันที่ลงรายการบัญชีใบแจ้งหนี้ 
    - **วันที่เอกสาร** – ระบุอัตราแลกเปลี่ยนตามวันที่เอกสารของสมุดรายวันการชำระเงิน ถ้าวันที่เอกสารของใบสำคัญว่างเปล่า จะมีการใช้วันที่การชำระเงิน

5. เลือก **บันทึก**

ถ้าสกุลเงินธุรกรรมแตกต่างจากสกุลเงินภาษีหัก ณ ที่จ่ายที่กําหนดไว้ในรหัสภาษีหัก ณ ที่จ่าย ยอดเงินในสกุลเงินภาษีหัก ณ ที่จ่ายจะถูกคํานวณจากสกุลเงินของธุรกรรม ตามการตั้งค่าก่อนหน้านี้ และจะถูกบันทึกในธุรกรรมภาษีหัก ณ ที่จ่ายที่ลงรายการบัญชีไว้
