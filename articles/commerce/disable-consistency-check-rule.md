---
title: ปิดใช้งานกฎในตัวตรวจสอบความสอดคล้องกันของธุรกรรมการขายปลีก
description: หัวข้อนี้อธิบายฟังก์ชันของการปิดใช้งานกฎในตัวตรวจสอบความสอดคล้องกันของธุรกรรมใน Microsoft Dynamics 365 Commerce
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5eb2af7e3090daabccd338d5d0bc6a6ebc4ea663
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982701"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>ปิดใช้งานกฎในตัวตรวจสอบความสอดคล้องกันของธุรกรรมการขายปลีก 

[!include [banner](../includes/banner.md)]

ผู้ขายปลีกอาจมีสถานการณ์และกระบวนการทางธุรกิจที่ไม่ซ้ำกัน ดังนั้นกฎทั้งหมดที่รวมไว้ตามค่าเริ่มต้นในตัวตรวจสอบความสอดคล้องกันของธุรกรรมการค้าจึงไม่สามารถใช้ได้กับผู้ขายปลีกทั้งหมด เพื่อรองรับความแตกต่าง Microsoft Dynamics 365 Commerce จึงมีฟังก์ชันที่สามารถใช้เพื่อปิดใช้งานกฎที่ไม่เกี่ยวข้องได้

เมื่อต้องการดูรายการของกฎที่มีอยู่ในตัวตรวจสอบความสอดคล้องกันของธุรกรรมในสภาพแวดล้อมของคุณ และเพื่อดูสถานะของกฎแต่ละรายการ ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์ Commerce** และเลือกแท็บ **การตรวจสอบความถูกต้องของธุรกรรม**

ตามค่าเริ่มต้น สถานะของกฎทั้งหมดตั้งค่าเป็น **เปิดใช้งาน** ดังนั้น จะมีการใช้งานกฎทั้งหมดเพื่อตรวจสอบความถูกต้องของธุรกรรมก่อนที่จะถูกดึงเข้าไปในใบแจ้งยอดการค้า เมื่อต้องการปิดใช้งานกฎ ให้เปลี่ยนสถานะเป็น **ปิดใช้งาน** กฎที่ถูกปิดใช้งานจะไม่ได้รับการพิจารณาเมื่อมีการตรวจสอบความถูกต้องของธุรกรรมระหว่างกระบวนการคำนวณของใบแจ้งยอด

เมื่อต้องการข้ามกระบวนการตรวจสอบความถูกต้องทั้งหมดโดยไม่คำนึงถึงกฎที่เปิดใช้งาน ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์ Commerce** จากนั้นแท็บ **การตรวจสอบความถูกต้องของธุรกรรม** ตั้งค่าตัวเลือก **ปิดใช้งานตัวตรวจสอบความสอดคล้องกันของธุรกรรมการค้า** เป็น **ใช่** หลังจากที่มีการตั้งค่าตัวเลือกนี้เป็น **ไม่** ตัวเลือกนี้จะไม่สามารถเปลี่ยนกลับเป็น **ใช่** จากอินเทอร์เฟสผู้ใช้ (UI)


[!INCLUDE[footer-include](../includes/footer-banner.md)]