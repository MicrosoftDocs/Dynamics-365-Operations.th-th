---
title: พารามิเตอร์การจัดซื้อและการจัดหาสำหรับต้นทุนแฝง
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าพารามิเตอร์การจัดซื้อและการจัดหาที่เกี่ยวข้อง เมื่อคุณใช้โมดูลต้นทุนแฝง
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccda3bd769a646e2390711883b8e40bec50e4d6a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020994"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="eaca3-103">พารามิเตอร์การจัดซื้อและการจัดหาสำหรับต้นทุนแฝง</span><span class="sxs-lookup"><span data-stu-id="eaca3-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eaca3-104">หน้า **พารามิเตอร์การจัดซื้อและการจัดหา** มีการตั้งค่าสองสามรายการที่เกี่ยวข้อง โดยเฉพาะเมื่อคุณใช้โมดูล **ต้นทุนแฝง**</span><span class="sxs-lookup"><span data-stu-id="eaca3-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="eaca3-105">ใช้กล่องโต้ตอบ **อัปเดตบรรทัดใบสั่ง** ที่เปิดจากหน้า **พารามิเตอร์การจัดซื้อและการจัดหา** เพื่อระบุว่าควรอัปเดตบรรทัดใบสั่งซื้อโดยอัตโนมัติหรือไม่ เมื่อมีการเปลี่ยนแปลงบนส่วนหัวของใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="eaca3-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="eaca3-106">เพื่อให้การตั้งค่านี้เสร็จสมบูรณ์ ให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="eaca3-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="eaca3-107">ไปที่ **การจัดซื้อและการจัดหา \> การตั้งค่า \> พารามิเตอร์การจัดซื้อและการจัดหา**</span><span class="sxs-lookup"><span data-stu-id="eaca3-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="eaca3-108">บนแท็บ **ทั่วไป** ให้เลือกลิงก์ **อัปเดตบรรทัดใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="eaca3-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="eaca3-109">กล่องโต้ตอบ **อัปเดตบรรทัดใบสั่ง** แสดงรายการฟิลด์บนส่วนหัวของใบสั่ง ที่สามารถใช้การอัปเดตอัตโนมัติกับฟิลด์ที่เกี่ยวข้องบนบรรทัดใบสั่งได้</span><span class="sxs-lookup"><span data-stu-id="eaca3-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="eaca3-110">ตั้งค่าแต่ละฟิลด์ในรายการให้เป็นหนึ่งในค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="eaca3-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="eaca3-111">**เสมอ** – บรรทัดใบสั่งควรอัปเดตโดยอัตโนมัติ เมื่อมีการอัพเดตส่วนหัวของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="eaca3-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="eaca3-112">**ไม่เคย** – บรรทัดใบสั่งควรไม่อัปเดต เมื่อมีการอัพเดตส่วนหัวของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="eaca3-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="eaca3-113">**พร้อมต์** – ผู้ใช้จะได้รับพร้อมต์เพื่อเลือกว่าควรจะอัปเดตบรรทัดใบสั่งหรือไม่</span><span class="sxs-lookup"><span data-stu-id="eaca3-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
