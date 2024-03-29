---
title: สถานการณ์ของวงเงินเครดิต
description: หัวข้อนี้จะอธิบายวิธีการตรวจสอบวงเงินเครดิตของลูกค้า เมื่อลูกค้าเป็นสมาชิกของกลุ่มวงเงินเครดิตของลูกค้า
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130267"
---
# <a name="credit-limit-scenarios"></a>สถานการณ์ของวงเงินเครดิต

ในการจัดการเครดิต คุณสามารถมอบหมายวงเงินเครดิตให้กับลูกค้าในระดับลูกค้าได้ คุณสามารถมอบหมายลูกค้าแต่ละคนให้กับ *กลุ่มวงเงินเครดิตของลูกค้า* และแต่ละกลุ่มมีวงเงินเครดิต ดังนั้น วงเงินเครดิตสามารถกำหนดให้กับลูกค้าในระดับกลุ่มได้ ลูกค้าทั้งหมดที่ได้รับมอบหมายให้กลุ่มเครดิตของลูกค้าเดียวกัน มีวงเงินเครดิตเหมือนกัน

โดยทั่วไป จะตรวจสอบวงเงินเครดิตของกลุ่มก่อนวงเงินเครดิตแต่ละรายการ วงเงินเครดิตแต่ละรายการไม่ได้แทนที่วงเงินเครดิตของกลุ่มเสมอ

บทความนี้จะอธิบายสถานการณ์ดังกล่าวห้าสถานการณ์ ที่เกี่ยวข้องกับกลุ่มเครดิตของลูกค้าและวงเงินเครดิตแต่ละตัว

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>วงเงินเครดิตของกลุ่มลูกค้า มากกว่าวงเงินเครดิตแต่ละรายการ

ตัวอย่างเช่น ลูกค้ามีวงเงินเครดิตแต่ละรายการ $10,000 ลูกค้าถูกกำหนดให้กับกลุ่มวงเงินเครดิตของลูกค้ และวงเงินเครดิตของกลุ่มนี้คือ $15,000 ในกรณีนี้ "วงเงินเครดิตที่มีผลบังคับใช้" ของลูกค้าคือ $10,000 เนื่องจากยอดเงินน้อยกว่าวงเงินกลุ่ม กฎการบล็อคจะตรวจสอบขีดจํากัดของกลุ่มก่อน จากนั้นจะตรวจสอบวงเงินแต่ละรายการ ใบสั่งขายที่เกิน $10,000 จะถูกบล็อค

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>วงเงินเครดิตของแต่ละราย มากกว่าวงเงินเครดิตของกลุ่มลูกค้า

ตัวอย่างเช่น ลูกค้ามีวงเงินเครดิตแต่ละรายการ $20,000 ลูกค้าถูกกำหนดให้กับกลุ่มวงเงินเครดิตของลูกค้ และวงเงินเครดิตของกลุ่มนี้คือ $15,000 ในกรณีนี้ "วงเงินเครดิตที่มีผลบังคับใช้" ของลูกค้าคือ $15,000 เนื่องจากกฎการบล็อคจะตรวจสอบวงเงินจำกัดของกลุ่มก่อนเสมอ ใบสั่งขายที่เกิน $15,000 จะถูกบล็อค

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>วงเงินเครดิตแต่ละรายการมีการตั้งค่าเป็น 0.00 และวงเงินสินเชื่อบังคับมีการตั้งค่าเป็น ใช่

ถ้าลูกค้ามีวงเงินเครดิตแต่ละรายการที่ตั้งค่าเป็น **0.00** และตัวเลือก **วงเงินเครดิตบังคับ** ถูกตั้งค่าเป็น **ใช่** วงเงินเครดิตที่มีผลบังคับใช้ของลูกค้าคือ $0.00 แม้ว่าลูกค้าจะถูกมอบหมายให้กับกลุ่มเครดิตของลูกค้า ด้วยวิธีนี้ ลูกค้าสามารถเป็นส่วนหนึ่งของกลุ่มได้ แต่ใบสั่งทั้งหมดจะไปที่การจัดการเครดิต

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>วงเงินเครดิตแต่ละรายการมีการตั้งค่าเป็น 0.00 และวงเงินเครดิตไม่จำกัด มีการตั้งค่าเป็น ใช่

ถ้าลูกค้ามีวงเงินเครดิตแต่ละรายการที่ตั้งค่าเป็น **0.00** แต่ตัวเลือก **วงเงินเครดิตไม่จำกัด** ถูกตั้งค่าเป็น **ใช่** ลูกค้าจะมีวงเงินเครดิตไม่จำกัด แม้ว่าจะถูกมอบหมายให้กับกลุ่มเครดิตของลูกค้า

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>วงเงินเครดิตแต่ละรายการถูกตั้งค่าเป็น 0.00 และลูกค้าเป็นส่วนหนึ่งของกลุ่มเครดิตของลูกค้า

ตัวอย่างเช่น ลูกค้ามีวงเงินสินเชื่อแต่ละรายการที่ตั้งค่าเป็น **0.00** ตัวเลือก **เครดิตไม่จำกัด** ถูกตั้งค่าเป็น **ไม่** และตัวเลือก **วงเงินเครดิตบังคับ** ถูกตั้งค่าเป็น **ไม่** ลูกค้าถูกกำหนดให้กับกลุ่มวงเงินเครดิตของลูกค้ และวงเงินเครดิตของกลุ่มนี้คือ $15,000 ในกรณีนี้ วงเงินเครดิตที่มีผลบังคับใช้ของลูกค้าคือวงเงินของกลุ่ม $15,000 ดังนั้น ใบสั่งขายที่เกินจํานวนนั้นจะถูกบล็อค ลักษณะการทงำานนี้ช่วยให้วงเงินเครดิตสามารถจัดการได้ในระดับกลุ่มเครดิตของลูกค้า แทนระดับลูกค้าแต่ละราย ลูกค้าทั้งหมดที่ได้รับมอบหมายให้กลุ่มเดียวกัน มีวงเงินเครดิตเหมือนกัน
