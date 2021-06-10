---
title: มิติทางการเงินและบัญชีหลักในภาษาที่เรียงจากขวาไปซ้าย
description: หัวข้อนี้อธิบายการตัดสินใจที่คุณจำเป็นต้องทำเมื่อคุณใช้ภาษาที่เรียงจากขวาไปซ้าย และคุณต้องตั้งค่ามิติทางการเงินและบัญชีหลัก
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 26fd186415db0adf01b8c53b188171fcf86fbc88
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111673"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="87f6d-103">มิติทางการเงินและบัญชีหลักในภาษาที่เรียงจากขวาไปซ้าย</span><span class="sxs-lookup"><span data-stu-id="87f6d-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87f6d-104">หัวข้อนี้อธิบายการตัดสินใจการนำไปใช้บางอย่างที่คุณควรพิจารณาเมื่อคุณใช้ภาษาที่เรียงจากขวาไปซ้าย และคุณต้องตั้งค่ามิติทางการเงินและบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="87f6d-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="87f6d-105">มิติทางการเงินและบัญชีหลักเป็นส่วนประกอบหลักของระยะการวางแผนสำหรับการนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="87f6d-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="87f6d-106">หลังจากที่มีการสร้างมิติทางการเงินและบัญชีหลักในระบบ รายการเหล่านั้นจะถูกใช้ในหน้า **ตั้งค่าคอนฟิกโครงสร้างทางบัญชี** **โครงสร้างกฎขั้นสูง** และ **การตั้งค่าคอนฟิกมิติทางการเงินสำหรับแอพลิเคชันการรวม**</span><span class="sxs-lookup"><span data-stu-id="87f6d-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="87f6d-107">ลำดับที่กำหนดในหน้าเหล่านั้นจะถูกใช้ในระบบเพื่อป้อนข้อมูลและปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="87f6d-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="87f6d-108">บางตำแหน่งในระบบ จะแสดงมิติทางการเงินและบัญชีหลักในฟิลด์ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="87f6d-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="87f6d-109">ในตำแหน่งอื่นๆ เช่น สมุดรายวัน มิติทางการเงินและบัญชีหลักจะปรากฏเป็นสตริงเดียว</span><span class="sxs-lookup"><span data-stu-id="87f6d-109">In other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="87f6d-110">แนวทางปฏิบัติสำหรับการตั้งค่ามิติทางการเงินและบัญชีหลักในระบบที่เรียงจากขวาไปซ้าย</span><span class="sxs-lookup"><span data-stu-id="87f6d-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

- <span data-ttu-id="87f6d-111">เมื่อคุณเลือกตัวกำหนดเขตสำหรับผังบัญชีแล้ว ให้เลือกตัวกำหนดเขตคู่ตัวเลือกใดตัวเลือกหนึ่ง: เครื่องหมายยัติภังค์สองเครื่องหมาย (`--`) แถบสองแถบ (`||`) หรือเครื่องหมายมหัพภาคสองเครื่องหมาย (`..`) หรือเครื่องหมายขีดเส้นใต้สองเครื่องหมาย (`\\`)</span><span class="sxs-lookup"><span data-stu-id="87f6d-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (`--`), double bar (`||`), double period (`..`), or double underscore (`\\`).</span></span>
- <span data-ttu-id="87f6d-112">เมื่อคุณสร้างค่ามิติทางการเงินและบัญชีหลัก ให้ใช้เฉพาะตัวเลขและอักขระของภาษาที่เรียงจากขวาไปซ้าย</span><span class="sxs-lookup"><span data-stu-id="87f6d-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
- <span data-ttu-id="87f6d-113">หลีกเลี่ยงการใช้ตัวกำหนดเขตผังบัญชีที่เลือกไว้ในค่ามิติทางการเงินและบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="87f6d-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="87f6d-114">โดยปฏิบัติตามแนวทางปฏิบัติเหล่านี้ คุณช่วยรับประกันการแสดงที่สอดคล้องกันของลำดับที่ผู้ใช้กำหนดทั่วทั้งระบบ</span><span class="sxs-lookup"><span data-stu-id="87f6d-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]