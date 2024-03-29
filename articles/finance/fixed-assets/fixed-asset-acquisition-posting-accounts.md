---
title: บัญชีการลงรายการการซื้อสินทรัพย์ถาวร
description: บทความนี้อธิบายวิธีการตั้งค่าบัญชีแยกประเภททั่วไป ที่ลงรายการบัญชีสำหรับสินทรัพย์ที่ซื้อสินทรัพย์
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: kfend
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93cbfc46fb41e47fba8b6cecf7811c0cf838e7d3
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719833"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a>บัญชีการลงรายการการซื้อสินทรัพย์ถาวร

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการตั้งค่าบัญชีแยกประเภททั่วไป ที่ลงรายการบัญชีสำหรับสินทรัพย์ที่ซื้อสินทรัพย์

บัญชีที่ใช้สำหรับการลงรายการการซื้อสินทรัพย์ถาวรอาจแตกต่างกันไป โดยขึ้นอยู่กับวิธีการที่ใช้เพื่อซื้อสินทรัพย์ ในหน้าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวรบนแท็บบัญชีแยกประเภท เลือกการซื้อสินทรัพย์ และการปรับปรุงการซื้อสินทรัพย์เพื่อตั้งค่าบัญชีสินทรัพย์ถาวรเพื่อลงรายการบัญชีในบัญชีแยกประเภท 

ในสมุดรายวัน และใบสั่งซื้อ บัญชีแยกประเภท คือบัญชีงบดุลที่ใช้โดยทั่วไป ซึ่งมีการเดบิตมูลค่าการซื้อของสินทรัพย์ถาวรใหม่ บัญชีนี้จะไม่แสดงในสมุดรายวัน และไม่สามารถแทนที่ในธุรกรรมได้ 

บัญชีตรงข้ามจะเป็นบัญชีงบดุลด้วย ในสมุดรายวันทั่วไป และ ในสมุดรายวันสินทรัพย์ถาวร บัญชีนี้มักจะเป็นบัญชีธนาคารที่ใช้ในการชำระค่าจ้างสำหรับการซื้อสินทรัพย์ บัญชีตรงข้ามเป็นบัญชีเริ่มต้น ซึ่งมีการแนะนำอยู่ในสมุดรายวัน สามารถเปลี่ยนในสมุดรายวันไปยังบัญชีอื่นใดจากผังบัญชี หรือไปยังบัญชีผู้จัดจำหน่าย ถ้าซื้อสินทรัพย์ถาวรมาจากผู้จัดจำหน่าย 

เมื่อใช้สมุดรายวันใบแจ้งหนี้หรือใบสั่งซื้อในบัญชี สำหรับการได้มาซึ่งสินทรัพย์ถาวร บัญชีตรงข้ามสำหรับธุรกรรมสินทรัพย์ถาวรจะถูกแทนที่ด้วยบัญชีผู้จัดจำหน่าย ที่เลือกไว้สำหรับธุรกรรมนั้น

สำหรับการลงรายการบัญชีการได้มาซึ่งสินทรัพย์ที่โดยใช้สมุดรายวันในบัญชีแยกประเภททั่วไป สินทรัพย์ถาวรไม่ได้ซื้อมาจากแหล่งภายนอก แต่โอนย้ายมาจากสินค้าคงคลังของบริษัทเอง ดังนั้น บัญชีตรงข้ามจึงเป็นบัญชีการตัดสินค้าจากคลังสำหรับสินค้าคงคลังในการบริหารสินค้าคงคลัง

สำหรับข้อมูลเพิ่มเติม ดู [ซื้อสินทรัพย์ผ่านการจัดซื้อ](acquire-assets-procurement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
