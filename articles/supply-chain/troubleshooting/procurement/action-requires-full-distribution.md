---
title: คุณสามารถทำให้การดำเนินการใบสั่งซื้อให้เสร็จสมบูรณ์ได้เฉพาะสำหรับหมายเลขรายการที่มีการกระจายทั้งหมดเท่านั้น
description: คุณสามารถทำให้การดำเนินการสั่งซื้อเสร็จสมบูรณ์ได้เฉพาะหลังจากที่หมายเลขรายการมีการกระจายทั้งหมดแล้วเท่านั้น
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1ef2a938a2a17bc2dbf38d09918eabdbccca8a28
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477778"
---
# <a name="you-can-only-complete-a-purchase-order-action-for-fully-distributed-line-numbers"></a>คุณสามารถทำให้การดำเนินการใบสั่งซื้อให้เสร็จสมบูรณ์ได้เฉพาะสำหรับหมายเลขรายการที่มีการกระจายทั้งหมดเท่านั้น

## <a name="symptom"></a>อาการ

คุณสามารถทำให้การดำเนินการสั่งซื้อเสร็จสมบูรณ์ได้เฉพาะหลังจากที่หมายเลขรายการมีการกระจายทั้งหมดแล้วเท่านั้น

## <a name="cause"></a>สาเหตุ

ปัญหานี้อาจเกิดขึ้นเนื่องจากความไม่สอดคล้องกันในการกระจายใบสั่งซื้อ

## <a name="resolution"></a>การแก้ปัญหา

เมื่อต้องการยกเลิกการบล็อกปัญหานี้และรีเซ็ตใบสั่งซื้อเป็นสถานะ *แบบร่าง* ให้ไปที่การ **จัดซื้อและการจัดหา \> งานประจำงวด \> ล้างข้อมูล \> รีเซ็ตการกระจายใบสั่งซื้อ** สำหรับข้อมูลเพิ่มเติมให้ดูที่การลงรายการบัญชีบล็อกต่อไปนี้: [แก้ไขข้อผิดพลาดในการกระจาย PO ใน Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/)
