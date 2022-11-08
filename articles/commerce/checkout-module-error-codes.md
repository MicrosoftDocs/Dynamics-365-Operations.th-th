---
title: รหัสอ้างอิงข้อผิดพลาดของโมดูลเช็คเอาท์
description: บทความนี้อธิบายถึงรหัสอ้างอิงข้อผิดพลาดของโมดูลเช็คเอาท์ซึ่งอยู่ในข้อความแสดงข้อผิดพลาดที่แสดงต่อผู้ใช้ใน Microsoft Dynamics 365 Commerce
author: BrianShook
ms.date: 10/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 952cb932522b4e0bb91be985e4f8974cb6cd8bc0
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728257"
---
# <a name="checkout-module-error-reference-codes"></a>รหัสอ้างอิงข้อผิดพลาดของโมดูลเช็คเอาท์

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

บทความนี้อธิบายถึงรหัสข้อผิดพลาดของโมดูลเช็คเอาท์ซึ่งอยู่ในข้อความแสดงข้อผิดพลาดที่แสดงต่อผู้ใช้ใน Microsoft Dynamics 365 Commerce

Dynamics 365 Commerce ได้แนะนําการอ้างอิงข้อผิดพลาดมาตรฐานที่สามารถรวมอยู่ในข้อผิดพลาดการเช็คเอาท์ของช่องทางออนไลน์ที่แสดงต่อลูกค้าออนไลน์ ใน Commerce รุ่น 10.0.31 และใหม่กว่า ข้อความแสดงข้อผิดพลาดในโมดูลเช็คเอาท์จะมีรหัสข้อผิดพลาดและไม่ต้องแสดงข้อมูลที่ไม่จําเป็นต่อลูกค้าออนไลน์ รหัสข้อผิดพลาดอ้างอิงถึงข้อผิดพลาดที่มีรายละเอียดอยู่ในบทความนี้

ตารางในบทความนี้มีรายละเอียดต่อไปนี้ ทั้งนี้ขึ้นอยู่กับข้อผิดพลาดที่พบ:

- คำอธิบายของเงื่อนไขที่เป็นสาเหตุให้เกิดข้อผิดพลาดหรือรายละเอียดเพิ่มเติม
- ข้อมูลสำหรับการพิจารณาในการตั้งค่าคอนฟิกสภาพแวดล้อมหรือตัวเชื่อมต่อการชำระเงิน
- ข้อมูลที่สามารถอ้างอิงในกรณีที่ขอรับการสนับสนุน หากต้องการความช่วยเหลือเพิ่มเติม

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

เมื่อต้องการเปิดใช้งานรหัสอ้างอิงข้อผิดพลาดของโมดูลเช็คเอาท์ที่แสดงรายการด้านล่าง ในโปรแกรมสร้างไซต์ของไซต์ของคุณ ให้ไปที่ **การตั้งค่าไซต์ \> ส่วนขยาย** และในส่วน **รถเข็นและการเช็คเอาท์** ให้เลือก **เปิดใช้งานการส่งข้อความแสดงข้อผิดพลาดของช่องทางออนไลน์ขั้นสูง** 

## <a name="checkout-module-error-reference-codes"></a>รหัสอ้างอิงข้อผิดพลาดของโมดูลเช็คเอาท์

ใช้ตารางต่อไปนี้เพื่อดูรายละเอียดเพิ่มเติมเกี่ยวกับการอ้างอิงรหัสข้อผิดพลาดซึ่งลูกค้าให้ไว้หรือประสบการณ์ในร้านค้าออนไลน์ เลื่อนไปทางขวาเพื่อดูคอลัมน์ **คำอธิบายข้อผิดพลาด**

| รหัสข้อผิดพลาด | รหัสข้อผิดพลาดที่เกี่ยวข้องกับ Dynamics | คำอธิบายข้อผิดพลาด |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | การชำระเงินไม่ได้รับอนุญาต ไม่มีรหัสชนิดบัตรใน **TokenizedPaymentCard** หรือรหัสชนิดบัตรที่ให้ไว้ไม่ได้รับการสนับสนุน |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | ถูกปฏิเสธ การชำระเงินไม่ได้รับอนุญาต |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | การชำระเงินไม่ได้รับอนุญาต ข้อมูลเพิ่มเติมที่ต้องการจากลูกค้า |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | ขออภัย มีบางอย่างผิดปกติ เราไม่สามารถขอรับผลลัพธ์การยอมรับการชำระเงินด้วยบัตร ลองอีกครั้งหรือติดต่อผู้ดูแลระบบของคุณ |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | ไม่สามารถดำเนินการชำระเงิน เนื่องจากคุณสมบัติการชำระเงินของผู้จำหน่ายขาดหายไป โปรดติดต่อผู้ดูแลระบบของคุณ |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | ไม่สามารถเรียกข้อมูลบริการชำระเงินสำหรับการดําเนินการ ตรวจสอบการตั้งค่าวิธีการจ่ายเงินของคุณสำหรับชนิดการชำระเงินที่เลือก |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | มีการใช้การชำระเงินด้วยบัญชีลูกค้าอยู่แล้วและอนุญาตให้ใช้การชำระเงินแบบเดียวเท่านั้นต่อธุรกรรม |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAmountDue | วงเงินบัญชีลูกค้าแตกต่างจากยอดเงินที่ต้องชำระ ลองใช้วิธีการชำระเงินแบบอื่นหรือติดต่อฝ่ายสนับสนุนลูกค้าเพื่อขอความช่วยเหลือ |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | การชำระเงินของบัญชีลูกค้าเกินยอดรวมที่ต้องชำระของสินค้าที่แสดง ลองอีกครั้งในภายหลังหรือติดต่อฝ่ายสนับสนุนลูกค้าสำหรับความช่วยเหลือ |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | การชำระเงินด้วยบัญชีลูกค้าต้องมีบัญชีของตนเองหรือมียอดเงินในใบแจ้งหนี้ที่ตรงกันในรายการชำระเงิน |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | ไม่สามารถจัดการกับการชำระเงินบัญชีของลูกค้าได้ในขณะนี้ – เกินมูลค่าวงเงิน |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | ลูกค้ารายนี้ไม่ได้รับอนุญาตให้ชำระเงินในบัญชี |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | ขออภัย มีบางอย่างผิดปกติ การชำระเงินไม่สามารถยกเลิกได้ ลองอีกครั้ง |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | เกิดข้อผิดพลาดขณะประมวลผลการชำระเงิน ลองอีกครั้งในภายหลัง |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | ยอดการชำระเงินของลูกค้าสมาชิกเกินยอดที่ได้รับอนุญาตสำหรับบัตรสมาชิกที่ใช้ในธุรกรรมนี้ |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | ยอดการขอคืนเงินของลูกค้าสมาชิกสำหรับธุรกรรมนี้เกินกว่าจำนวนที่อนุญาตในบัตรสมาชิก |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | ไม่พบหมายเลขบัตรสมาชิก เปิดใช้งานหมายเลขบัตรสมาชิกหรือป้อนหมายเลขบัตรสมาชิกอื่น แล้วลองอีกครั้ง |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | ไม่มีหมายเลขบัตรสมาชิก ป้อนหมายเลขบัตรสมาชิกอื่น แล้วลองอีกครั้ง |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | บัตรสมาชิกใบนี้ไม่สามารถใช้แลกคะแนนสะสมสำหรับสมาชิกในธุรกรรมนี้ |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | พบข้อผิดพลาดกับหมายเลขบัตรของขวัญ ลองใช้บัตรของขวัญอื่นหรือติดต่อฝ่ายสนับสนุนลูกค้าเพื่อขอความช่วยเหลือ |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | ยอดเงินเกินกว่ายอดคงเหลือในบัตรของขวัญ ป้อนยอดเงินอื่น แล้วลองอีกครั้ง |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | ธุรกรรมไม่สามารถมีรายการในการชำระเงินของสมาชิกมากกว่าหนึ่งรายการ |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | ข้อมูลการชำระเงินขาดหายไปหรือไม่ถูกต้อง ตรวจสอบข้อมูลการชำระเงิน แล้วลองอีกครั้ง |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | ไม่สามารถดำเนินการกับใบสั่งได้ในขณะนี้ ลองอีกครั้งในภายหลัง |
| CCR025     | ส่วนหน้าหมดเวลาสำหรับ API การเช็คเอาท์ | การดําเนินการของส่วนหน้าหมดเวลา ยืนยันว่าใบสั่งได้รับการดำเนินการใน Dynamics 365 Commerce headquarters หรือไม่ |
| CCR026     | เปลี่ยนแปลงยอดเงินที่อนุมัติของเดิมแล้ว | ยอดเงินในใบสั่งมีการเปลี่ยนแปลงจากยอดเงินการที่อนุมัติของเดิมที่ดำเนินการด้วยเกตเวย์การชำระเงิน การดำเนินการนี้อาจเกิดจากการหมดอายุของคูปอง โปรโมชัน หรือการขาย |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | เกิดข้อผิดพลาดขณะประมวลผลการชำระเงิน การอ้างอิงที่ให้กับ API รถเข็นเป็นการอ้างอิงที่แตกต่างจากที่คาดไว้ (dkiไม่สอดคล้องกันที่อาจเกิดขึ้นระหว่างกระบวนการเช็คเอาท์) |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | วิธีการชำระเงินที่ลองใช้เกิดข้อผิดพลาด ติดต่อฝ่ายสนับสนุนเพื่อตรวจสอบการตั้งค่าบัญชีของคุณ หรือลองอีกครั้งด้วยวิธีการชำระเงินอื่น |

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[คำถามที่ถามบ่อยเกี่ยวกับการชำระเงิน](dev-itpro/payments-retail.md)

[โมดูลเช็คเอาท์](add-checkout-module.md)

[โมดูลการชำระเงิน](payment-module.md)
