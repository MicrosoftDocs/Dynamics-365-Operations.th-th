---
title: ตั้งค่ากำหนดการชำระเงินด้วยการปันส่วน TDS
description: บทความนี้อธิบายวิธีการตั้งค่ากำหนดการชำระเงินด้วยการปันส่วนภาษี ณ ที่จ่าย (TDS)
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 48891c32f39b743ce26e265c5682dab28ecb4b27
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868325"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>ตั้งค่ากำหนดการชำระเงินด้วยการปันส่วน TDS

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการตั้งค่ากำหนดการชำระเงินด้วยการปันส่วนภาษี ณ ที่จ่าย (TDS)

1. ไปที่ **บัญชีเจ้าหนี้ \> การตั้งค่าการชำระเงิน \> กำหนดการชำระเงิน**

    [![หน้ากำหนดการชำระเงิน](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. ในบานหน้าต่างการดำเนินการ เลือก **ใหม่** เพื่อสร้างกำหนดการชำระเงิน และป้อนรายละเอียดที่จำเป็น
3. ในฟิลด์ **การปันส่วน** เลือกวิธีที่จะปันส่วนการชำระเงินสำหรับกำหนดการชำระเงิน:

    - ผลรวม
    - ยอดเงินคงที่
    - ปริมาณคงที่
    - ที่ระบุ

    ฟิลด์ **การปันส่วนภาษีหัก ณ ที่จ่าย** แสดงวิธีการปันส่วน TDS สำหรับกำหนดการชำระเงิน ถ้าคุณเลือก **ผลรวม** ในฟิลด์ **การปันส่วน** ฟิลด์ **การปันส่วนภาษีหัก ณ ที่จ่าย** จะถูกตั้งค่าเป็น **ผลรวม** โดยอัตโนมัติ ถ้าคุณเลือก **ยอดเงินคงที่** **ปริมาณคงที่** หรือ **ที่ระบุ** ในฟิลด์ **การปันส่วน** ฟิลด์ **การปันส่วน ภาษีหัก ณ ที่จ่าย** จะถูกตั้งค่าเป็น **ตามสัดส่วน** โดยอัตโนมัติ

    > [!NOTE]
    > หากฟิลด์ **การปันส่วนภาษีหัก ณ ที่จ่าย** มีการตั้งค่าเป็น **ยอดรวม** งวดการชำระเงินจะคำนวณตามยอดเงินรวม ซึ่งรวมถึงยอดเงิน TDS ด้วย หากฟิลด์ **การปันส่วนภาษีหัก ณ ที่จ่าย** มีการตั้งค่าเป็น **ตามสัดส่วน** งวดการชำระเงินจะคำนวณตามยอดเงินสุทธิตามใบแจ้งหนี้ หลังหักยอดเงิน TDS

4. ป้อนรายละเอียดอื่นๆ ที่จำเป็น แล้วปิดหน้า
