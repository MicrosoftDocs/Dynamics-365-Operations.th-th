---
title: การตั้งค่าหลักการตัดจ่ายบนบรรทัด BOM ไม่ได้รับการยอมรับ
description: การตั้งค่าหลักการตัดจ่ายบนบรรทัดสูตรการผลิต (BOM) ไม่ได้รับการยอมรับ
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026951"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="9c4b1-103">การตั้งค่าหลักการตัดจ่ายบนบรรทัด BOM ไม่ได้รับการยอมรับ</span><span class="sxs-lookup"><span data-stu-id="9c4b1-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="9c4b1-104">หมายเลข KB: 4612725</span><span class="sxs-lookup"><span data-stu-id="9c4b1-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="9c4b1-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="9c4b1-105">Symptoms</span></span>

<span data-ttu-id="9c4b1-106">ปัญหานี้จะเกิดขึ้นเมื่อตั้งค่าฟิลด์ **การใช้ BOM อัตโนมัติ** บนแท็บ **การอัปเดตอัตโนมัติ** ของหน้า **พารามิเตอร์การควบคุมการผลิต** เป็น *หลักการตัดจ่าย*</span><span class="sxs-lookup"><span data-stu-id="9c4b1-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="9c4b1-107">การตั้งค่านี้บ่งชี้ว่าบรรทัดสูตรการผลิต (BOM) ทั้งหมดควรใช้โดยอัตโนมัติเมื่อได้รับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="9c4b1-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="9c4b1-108">ถ้าฟิลด์ **หลักการตัดจ่าย** บนรายการ BOM มีการตั้งค่าไว้อย่างชัดแจ้งเป็น *ด้วยตนเอง* คุณอาจคาดว่ารายการ BOM จะไม่ถูกใช้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9c4b1-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="9c4b1-109">อย่างไรก็ตาม เมื่อปัญหานี้เกิดขึ้น รายการ BOM ที่มีการตั้งค่าฟิลด์ **หลักการตัดจ่าย** เป็น *ด้วยตนเอง* โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9c4b1-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="9c4b1-110">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="9c4b1-110">Resolution</span></span>

<span data-ttu-id="9c4b1-111">ถ้าคุณประสบปัญหานี้อยู่ อาจมีการตั้งค่าพารามิเตอร์การควบคุมการผลิตของคุณแทนที่การตั้งค่า **หลักการตัดจ่าย** บนรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="9c4b1-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="9c4b1-112">บนหน้า **พารามิเตอร์การควบคุมการผลิต** บนแท็บ **การอัปเดตอัตโนมัติ** ให้ตรวจสอบค่าของฟิลด์ **ปริมาณการใช้ BOM แบบอัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="9c4b1-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="9c4b1-113">ถ้ามีการตั้งค่าเป็น *เสมอ* ระบบจะละเว้นการตั้งค่า **หลักการตัดจ่าย** บนรายการ BOM ทั้งหมดและจะล้างรายการเสมอ</span><span class="sxs-lookup"><span data-stu-id="9c4b1-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="9c4b1-114">เพื่อให้ระบบปฏิบัติตามการตั้งค่า **หลักการตัดจ่าย** บนรายการ BOM ให้เปลี่ยนค่าของฟิลด์ **ปริมาณการใช้ BOM แบบอัตโนมัติ** เป็น *หลักการตัดจ่าย*</span><span class="sxs-lookup"><span data-stu-id="9c4b1-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
