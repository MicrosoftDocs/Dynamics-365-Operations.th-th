---
title: มีการชำระเงินโดยอัตโนมัติก่อนออกใบแจ้งหนี้หรือจัดส่งสินค้าตามใบสั่ง
description: บทความนี้มีแนวทางการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อมีการจ่ายเงินในพอร์ทัล Adyen ทันทีหลังจากที่วางใบสั่ง ถึงแม้ว่าใบสั่งขายจะยังไม่ได้ออกใบแจ้งหนี้หรือจัดส่งสินค้า
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c01a2fda54e198a43fa84ae83686fc1701958b6b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890280"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>มีการชำระเงินโดยอัตโนมัติก่อนออกใบแจ้งหนี้หรือจัดส่งสินค้าตามใบสั่ง

[!include [banner](../../includes/banner.md)]

บทความนี้มีแนวทางการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อมีการจ่ายเงินในพอร์ทัล Adyen ทันทีหลังจากที่วางใบสั่ง ถึงแม้ว่าใบสั่งขายจะยังไม่ได้ออกใบแจ้งหนี้หรือจัดส่งสินค้า

## <a name="description"></a>คำอธิบาย

หลังจากสั่งซื้อแล้ว การชำระเงินจะชำระทันทีในพอร์ทัล Adyen ถึงแม้ว่าใบสั่งขายจะยังไม่ได้ออกใบแจ้งหนี้หรือจัดส่งสินค้า

## <a name="resolution"></a>ความละเอียด

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>ตั้งค่าคอนฟิกการรวบรวมข้อมูลด้วยตนเองสำหรับการชำระเงินอีคอมเมิร์ซ ในพอร์ทัล Adyen

ตั้งค่าคอนฟิกการรวบรวมข้อมูลด้วยตนเองสำหรับการชำระเงินอีคอมเมิร์ซ ในพอร์ทัล Adyen ให้ทำตามขั้นตอนดังต่อไปนี้

1. ลงชื่อเข้าใช้ พอร์ทัล Adyen
1. ในมุมขวาบน ให้เลือกบัญชีผู้ขายของคุณให้กับช่องทางอีคอมเมิร์ซ
1. บนแถบนำทางบนสุด ให้เลือก **บัญชี** แล้วจากนั้นเลือก **การตั้งค่า**
1. ในฟิลด์ **ความล่าช้าในการรวบรวมข้อมูล** ให้เลือก **ด้วยตนเอง**

    ![การตั้งค่าความล่าช้าในการรวบรวมข้อมูลในพอร์ทัล Adyen](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[การรวบรวมข้อมูลการชำระเงิน Adyen](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 Payment Connector สำหรับ Adyen](../dev-itpro/adyen-connector.md)

[ตั้งค่าตัวเชื่อมต่อการชำระเงิน Adyen สำหรับ Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
