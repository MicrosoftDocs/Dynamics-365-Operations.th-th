---
title: สร้างงบประมาณจากบัญชีธุรกรรมและบัญชีผลรวม
description: บทความนี้แสดงภาพรวมของกระบวนการสร้างงบประมาณที่ขึ้นอยู่กับบัญชีผลรวม นอกจากนี้ยังอธิบายวิธีการเปิดการควบคุมงบประมาณสำหรับบัญชีผลรวม ถ้าจำเป็นต้องมีการควบคุมงบประมาณ
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c2298a774e35bc92fafb8bc24871b288fb198d7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003092"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>สร้างงบประมาณจากบัญชีธุรกรรมและบัญชีผลรวม

[!include [banner](../includes/banner.md)]

บทความนี้แสดงภาพรวมของกระบวนการสร้างงบประมาณที่ขึ้นอยู่กับบัญชีผลรวม นอกจากนี้ยังอธิบายวิธีการเปิดการควบคุมงบประมาณสำหรับบัญชีผลรวม ถ้าจำเป็นต้องมีการควบคุมงบประมาณ

ทั้งเอกสารแผนงบประมาณและเอกสารรายการทะเบียนงบประมาณที่อนุญาตสำหรับการจัดทำงบประมาณบนบัญชีหลักที่มีชนิดบัญชีหลักของ **ผลรวม** สามารถลงรายการบัญชีที่เกิดขึ้นจริงกับธุรกรรมบัญชีหลักเท่านั้น 

สำหรับกระบวนการประจำงวด **การสร้างแผนงบประมาณจากบัญชีแยกประเภททั่วไป** บนแท็บ **แหล่งที่มา** คุณสามารถระบุชนิดบัญชีหลักเป็น **ผลรวม** เป็นเงื่อนไขได้ ในกรณีนี้ แต่ละผลรวมบัญชีหลักจะรวมอยู่ในแผนงบประมาณเป้าหมาย และยอดเงินจะเท่ากับจำนวนรวมของช่วงบัญชีหลักที่เลือก 

คุณสามารถเรียกใช้การควบคุมงบประมาณสำหรับบัญชีหลักของชนิด **ผลรวม** ฟังก์ชันนี้ได้รับการสนับสนุนผ่านการใช้กลุ่มงบประมาณ สำหรับแต่ละผลรวมบัญชีหลัก คุณต้องสร้างงบประมาณที่ควรถูกควบคุมสำหรับกลุ่มงบประมาณในหน้า **การตั้งค่าคอนฟิกการควบคุมงบประมาณ** เงื่อนไขที่คุณระบุต้องรวมผลรวมบัญชีหลักและช่วงของบัญชี เมื่อต้องการเพิ่มความเร็วกระบวนการการสร้างกลุ่มงบประมาณ คุณสามารถใช้ประโยชน์ของเอนทิตี้ข้อมูลของกลุ่มการควบคุมงบประมาณ 

เมื่อใช้งบประมาณในการรายงาน ตัวอย่างเช่น บนงบการเงิน ผลรวมของงบประมาณสำหรับบัญชีผลรวมจะประกอบด้วยจำนวนดังนี้:

-   งบประมาณที่ถูกสร้างจากธุรกรรมบัญชีแยกประเภทแต่ละบัญชีภายในช่วงของบัญชีผลรวม
-   จำนวนเงินงบประมาณถูกป้อนโดยตรงในบัญชีผลรวม

ดังนั้น คุณสามารถสร้างงบประมาณที่แยกกันสำหรับบัญชีธุรกรรมที่สำคัญที่สุดในช่วงของบัญชีผลรวม และเพิ่มจำนวนเงินงบประมาณที่พร้อมใช้ให้กับบัญชีผลรวมได้



