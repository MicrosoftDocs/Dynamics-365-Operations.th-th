---
title: ตั้งค่าหน่วยงานจัดเก็บภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS
description: บทความนี้อธิบายวิธีการตั้งค่าหน่วยงานจัดเก็บภาษีที่หักที่ต้นทาง (TDS)
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
ms.openlocfilehash: 43562381bab93d2f143788b8dc61f2b13d05db3b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864226"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a>ตั้งค่าหน่วยงานจัดเก็บภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการตั้งค่าหน่วยงานจัดเก็บภาษีที่หักที่ต้นทาง (TDS)

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
