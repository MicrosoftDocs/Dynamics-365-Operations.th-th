---
title: คุณสามารถเพิ่มได้เฉพาะบัญชีหลักเป็นบัญชีเครดิตเพื่อเหตุผลการกระทบยอดเท่านั้น
description: เมื่อคุณตั้งค่าเหตุผลการกระทบยอดในการจัดการการขนส่ง คุณสามารถเพิ่มเฉพาะบัญชีหลักเป็นบัญชีเครดิตเท่านั้น
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026935"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="8aade-103">คุณสามารถเพิ่มได้เฉพาะบัญชีหลักเป็นบัญชีเครดิตเพื่อเหตุผลการกระทบยอดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8aade-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="8aade-104">หมายเลข KB: 4603538</span><span class="sxs-lookup"><span data-stu-id="8aade-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="8aade-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="8aade-105">Symptoms</span></span>

<span data-ttu-id="8aade-106">เมื่อคุณตั้งค่าเหตุผลการกระทบยอดในการจัดการการขนส่ง คุณสามารถเพิ่มเฉพาะบัญชีหลักเป็นบัญชีเครดิตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8aade-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="8aade-107">คุณไม่สามารถเพิ่มศูนย์ต้นทุนหรือมิติอื่นใดเป็นบัญชีเครดิต</span><span class="sxs-lookup"><span data-stu-id="8aade-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="8aade-108">อย่างไรก็ตาม บัญชีเดบิตอนุญาตให้คุณเลือกมิติอื่น</span><span class="sxs-lookup"><span data-stu-id="8aade-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="8aade-109">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="8aade-109">Resolution</span></span>

<span data-ttu-id="8aade-110">ถ้าการกระทบยอดยังไม่เสร็จสิ้นเพื่อจ่ายเงินให้แก่ผู้จัดจำหน่าย แต่ในการเครดิตบัญชีหลักที่ระบุ ระบบจะไม่อนุญาตให้คุณเลือกมิติทางการเงินให้กับบัญชีเครดิตเมื่อคุณตั้งค่าเหตุผลการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="8aade-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="8aade-111">ถ้าโครงสร้างทางบัญชีต้องการค่ามิติทางการเงินเฉพาะให้กับบัญชีหลักเครดิต จึงไม่สามารถลงรายการบัญชีสมุดรายวันผู้จัดจำหน่ายที่เป็นผลลัพธ์โดยอัตโนมัติได้ เนื่องจากค่ามิติทางการเงินขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="8aade-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="8aade-112">ดังนั้น คุณต้องระบุบัญชีเครดิตด้วยตนเองโดยใช้หน้า **สมุดรายวันใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="8aade-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="8aade-113">เนื่องจากต้องระบุค่ามิติที่บัญชีเครดิต คุณไม่สามารถลงรายการบัญชีสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่ายโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="8aade-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="8aade-114">คุณต้องลงรายการบัญชีด้วยตนเองหลังจากที่คุณเพิ่มค่ามิติในบัญชีหลักให้กับรายการเครดิตด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="8aade-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
