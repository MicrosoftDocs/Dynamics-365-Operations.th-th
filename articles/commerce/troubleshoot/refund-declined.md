---
title: การขอคืนเงินของใบสั่งส่งคืนสินค้าได้รับการปฏิเสธ
description: หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อมีการปฏิเสธการขอคืนเงินในใบสั่งส่งคืนสินค้า เนื่องจากบัตรเครดิตที่ใช้สําหรับการออกใบแจ้งหนี้แตกต่างจากบัตรที่ใช้ในระหว่างการตรวจสอบการออกใบแจ้งหนี้ดั้งเดิม
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
ms.openlocfilehash: 89fe41d7ce57b584be34b156696b4044c4571afe
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347283"
---
# <a name="refund-on-a-return-order-is-declined"></a>การขอคืนเงินของใบสั่งส่งคืนสินค้าได้รับการปฏิเสธ

[!include [banner](../../includes/banner.md)]

หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อมีการปฏิเสธการขอคืนเงินในใบสั่งส่งคืนสินค้า เนื่องจากบัตรเครดิตที่ใช้สําหรับการออกใบแจ้งหนี้แตกต่างจากบัตรที่ใช้ในระหว่างการตรวจสอบการออกใบแจ้งหนี้ดั้งเดิม

## <a name="description"></a>คำอธิบาย

การขอคืนเงินได้รับการปฏิเสธเมื่อบัตรเครดิตที่ใช้ในการออกใบแจ้งหนี้ใบสั่งส่งคืนสินค้าแตกต่างจากบัตรที่ใช้ในระหว่างการอนุมัติการชำระเงินครั้งแรก คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "การชำระเงินบางรายการไม่อยู่ในสถานะที่ถูกต้องในการลงรายการบัญชี โปรดตรวจสอบความถูกต้องของสถานะการชำระเงินทั้งหมดอีกครั้งก่อนการออกใบแจ้งหนี้"

รายละเอียดการตรวจสอบการชำระเงินจะรวมข้อความแสดงข้อผิดพลาดต่อไปนี้: "เกตเวย์ Adyen SendRequest() ล้มเหลวโดยมีสถานะ 'InternalServerError'.22144; การตอบสนองว่างเปล่าที่ส่งคืนจาก Adyen (22001);"

![ข้อผิดพลาดการขอคืนเงินที่ถูกปฏิเสธในใบสั่งส่งคืนสินค้า](media/refund-order-decline.jpg)

## <a name="resolution"></a>การแก้ปัญหา

### <a name="enable-blind-returns-in-adyen"></a>เปิดใช้งานการส่งคืนที่ซ่อนใน Adyen

หากต้องการเปิดใช้งานการส่งคืนที่ซ่อนอยู่ ให้ปฏิบัติตามขั้นตอนใน [การแก้ไขปัญหาข้อผิดพลาดเกี่ยวกับ Dynamics 365 Payment Connector ของปัญหา Adyen](adyen-support.md) เพื่อติดต่อทีมสนับสนุน Adyen และขอให้เปิดใช้งานการส่งคืนที่ซ่อนอยู่บนบัญชีร้านค้า Adyen ของคุณ

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen](../dev-itpro/adyen-connector.md)

[ตั้งค่าตัวเชื่อมต่อการชำระเงิน Adyen สำหรับ Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
