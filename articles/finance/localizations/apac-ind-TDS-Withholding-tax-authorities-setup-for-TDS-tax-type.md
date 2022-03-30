---
title: ตั้งค่าหน่วยงานจัดเก็บภาษีหัก ณ ที่จ่ายในชนิดภาษี TDS
description: หัวข้อนี้อธิบายวิธีการตั้งค่าหน่วยงานจัดเก็บภาษีที่หักที่ต้นทาง (TDS)
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: a9b6105c227b530f0cd7a932aac18e8942482d12
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408266"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a>ตั้งค่าหน่วยงานจัดเก็บภาษีหัก ณ ที่จ่ายในชนิดภาษี TDS

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการตั้งค่าหน่วยงานจัดเก็บภาษีที่หักที่ต้นทาง (TDS)

1. ไปที่ **ภาษี \> ภาษีทางอ้อม \> หน่วยงานจัดเก็บภาษีหัก ณ ที่จ่าย**

    [![หน้าหน่วยงานจัดเก็บภาษีหัก ณ ที่จ่าย](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)

2. ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS** เพื่อตั้งค่าหน่วยงานจัดเก็บภาษีหัก ณ ที่จ่ายให้กับชนิดภาษี TDS
3. ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างรายการ
4. ในฟิลด์ **หน่วยงานจัดเก็บภาษีหัก ณ ที่จ่าย** ให้ป้อนชื่อสำหรับหน่วยงานจัดเก็บภาษี TDS
5. ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
6. ใน FastTab **General** ในฟิลด์ **บัญชีผู้จัดจำหน่าย** เลือกบัญชีผู้จัดจำหน่ายสำหรับหน่วยงานจัดเก็บภาษี TDS

    > [!NOTE]
    > คุณต้องกําหนดชื่อของธนาคารที่ซึ่งเงินฝากธนาคารที่เป็นหนี้ผู้จัดจำหน่ายของหน่วยงานจัดเก็บภาษี TDS จะถูกฝากไว้ ชื่อของธนาคารจะถูกกําหนดอยู่ในหน้า **บัญชีธนาคาร** (**บัญชีเจ้าหนี้ \> ผู้จัดจำหน่ายทั้งหมด \> ผู้จัดจำหน่าย \> การตั้งค่า \> บัญชีธนาคาร**)

7. ปิดหน้า
