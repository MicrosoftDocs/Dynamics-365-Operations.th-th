---
title: คุณไม่สามารถออกใบแจ้งหนี้ใบสั่งขายที่เชื่อมต่อกับลูกค้าได้
description: คุณไม่สามารถออกใบแจ้งหนี้ใบสั่งขายต้นฉบับและใบสั่งซื้อต้นฉบับโดยตรงได้อีกต่อไปหลังจากที่คุณเปิดใช้งานตัวเลือกลงรายการบัญชีใบแจ้งหนี้โดยอัตโนมัติ
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026945"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="71412-103">คุณไม่สามารถออกใบแจ้งหนี้ใบสั่งขายที่เชื่อมต่อกับลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="71412-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="71412-104">หมายเลข KB: 4611793</span><span class="sxs-lookup"><span data-stu-id="71412-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="71412-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="71412-105">Symptoms</span></span>

<span data-ttu-id="71412-106">คุณไม่สามารถออกใบแจ้งหนี้ใบสั่งขายต้นฉบับและใบสั่งซื้อต้นฉบับโดยตรงได้อีกต่อไปหลังจากที่คุณเปิดใช้งานตัวเลือก  **ลงรายการบัญชีใบแจ้งหนี้โดยอัตโนมัติ** บนหน้า **ระหว่างบริษัท** สำหรับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="71412-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="71412-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="71412-107">Resolution</span></span>

<span data-ttu-id="71412-108">ลักษณะการซิงโครไนส์ของใบแจ้งหนี้ใบสั่งระหว่างบริษัทและใบแจ้งหนี้ใบสั่งการจัดส่งโดยตรงจะถูกควบคุมและบังคับโดยพารามิเตอร์ที่อธิบายไว้ใน [ตั้งค่าพารามิเตอร์เพื่อลงรายการบัญชีใบสั่งระหว่างบริษัท](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order)</span><span class="sxs-lookup"><span data-stu-id="71412-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="71412-109">หลังจากที่คุณตั้งค่าพารามิเตอร์เหล่านั้นแล้ว คุณต้องออกใบแจ้งหนี้ใบสั่งขายระหว่างบริษัทก่อน</span><span class="sxs-lookup"><span data-stu-id="71412-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="71412-110">จากนั้นจะมีการซิงโครไนส์ใบสั่งขายและใบสั่งซื้อต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="71412-110">The original sales orders and purchase orders will then be synchronized.</span></span>
