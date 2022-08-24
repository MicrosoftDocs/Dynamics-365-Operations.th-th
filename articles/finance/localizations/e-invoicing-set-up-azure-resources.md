---
title: ตั้งค่าทรัพยากร Azure สำหรับการออกใบแจ้งหนี้อิเล็กทรอนิกส์
description: บทความนี้แสดงภาพรวมของกระบวนการสำหรับการตั้งค่าทรัพยากร Microsoft Azure สำหรับการออกใบแจ้งหนี้อิเล็กทรอนิกส์
author: gionoder
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f11e4eac831d54a6cac765a5adc4e4ffddbe0a22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283099"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>ตั้งค่าทรัพยากร Azure สำหรับการออกใบแจ้งหนี้อิเล็กทรอนิกส์

[!include [banner](../includes/banner.md)]

กระบวนการสำหรับการตั้งค่าทรัพยากร Microsoft Azure สำหรับการออกใบแจ้งหนี้อิเล็กทรอนิกส์มีสามขั้นตอน สองขั้นตอนแรก "สร้าง Azure Key Vault ในพอร์ทัล Azure" และ "สร้างบัญชีที่เก็บข้อมูล Azure ในพอร์ทัล Azure" ถือเป็นข้อบังคับ ขั้นตอนที่สาม "ตั้งค่าคอนฟิกการเชื่อมต่อ SharePoint" ไม่บังคับ

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>สร้าง Azure Key Vault ในพอร์ทัล Azure

สร้าง Key Vault ในการสมัครใช้งาน Azure ของคุณ ขอแนะนำว่าคุณควรสร้าง Key Vault แยกต่างหากสำหรับการออกใบแจ้งหนี้อิเล็กทรอนิกส์ และไม่ควรรวมข้อมูลลับนี้กับแอปพลิเคชันอื่น สร้างข้อมูลลับและใบรับรองได้มากที่สุดเท่าที่คุณต้องการสำหรับสถานการณ์ของคุณในเอกสารอิเล็กทรอนิกส์ คุณต้องสร้างข้อมูลลับอย่างน้อยหนึ่งรายการเพื่อจัดเก็บโทเค็นลายเซ็นการเข้าถึงที่ใช้ร่วมกัน (SAS) ของบัญชีที่เก็บข้อมูล Azure ที่คุณจะสร้างในขั้นตอนถัดไป

สำหรับข้อมูลเกี่ยวกับวิธีการทำตามขั้นตอนนี้ ดูที่ [สร้าง Azure Key Vault ในพอร์ทัล Azure](e-invoicing-create-azure-key-vault-azure-portal.md)

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>สร้างบัญชีที่เก็บข้อมูล Azure ในพอร์ทัล Azure

คุณเป็นเจ้าของเอกสารและไฟล์อิเล็กทรอนิกส์ทั้งหมดที่สร้างขึ้นโดยบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์หรือเข้าสู่บริการ เอกสารและไฟล์เหล่านั้นจัดเก็บอยู่ในบัญชีที่เก็บข้อมูล Azure ที่คุณสร้างในการสมัครใช้งาน Azure ของคุณ บริการดังกล่าวจะเข้าถึงบัญชีที่เก็บข้อมูลของคุณโดยใช้โทเค็น SAS ที่ได้จากข้อมูลลับ Key Vault ของคุณ

สำหรับข้อมูลเกี่ยวกับวิธีการทำตามขั้นตอนนี้ ดูที่ [สร้างบัญชีที่เก็บข้อมูล Azure ในพอร์ทัล Azure](e-invoicing-create-azure-storage-account-azure-portal.md)

## <a name="configure-a-sharepoint-connection"></a>ตั้งค่าคอนฟิกการเชื่อมต่อ SharePoint

ในบางสถานการณ์ คุณอาจต้องบันทึกไฟล์อิเล็กทรอนิกส์ไปยัง SharePoint และเรียกข้อมูลจาก SharePoint เพื่อให้แน่ใจว่าบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์สามารถเข้าถึงโฟลเดอร์ SharePoint ของคุณ ให้ตั้งค่าคอนฟิกการเข้าถึง SharePoint

สำหรับข้อมูลเกี่ยวกับวิธีการทำตามขั้นตอนนี้ ดูที่ [ตั้งค่าคอนฟิกการเชื่อมต่อ SharePoint](e-invoicing-create-sharepoint-connection.md)
