---
title: อัปเกรดสมุดรายวันใบสำคัญเดียวและการประเมินค่าใหม่ตามสกุลเงิน
description: หัวข้อนี้อธิบายวิธีอัปเกรดสมุดรายวันใบสำคัญเดียวและการประเมินค่าใหม่ตามสกุลเงิน
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb4eca4933716105789d3bbc21dd374395211d1d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559532"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="2a066-103">อัปเกรดสมุดรายวันใบสำคัญเดียวและการประเมินค่าใหม่ตามสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="2a066-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a066-104">บางองค์กรป้อนสมุดรายวันที่ประกอบด้วยใบสำคัญเดียวที่มีลูกค้าหรือผู้จัดจำหน่ายมากกว่าหนึ่งราย และยังเรียกใช้กระบวนการประเมินค่าใหม่ตามสกุลเงินต่างประเทศสำหรับบัญชีลูกหนี้หรือบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2a066-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="2a066-105">หัวข้อนี้อธิบายถึงขั้นตอนที่องค์กรเหล่านี้ควรปฏิบัติตามเมื่อจะปรับรุ่นเป็น Microsoft Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="2a066-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="2a066-106">ทำตามขั้นตอนเหล่านี้เมื่อคุณอัพเกรดเป็น Microsoft Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="2a066-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="2a066-107">ก่อนที่คุณจะปรับรุ่นเป็น Finance and Operations ให้เรียกใช้กระบวนการประเมินค่าใหม่ตามสกุลเงินต่างประเทศสำหรับบัญชีลูกหนี้และบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2a066-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="2a066-108">ตั้งค่าฟิลด์ **วิธีการ** เป็น **วันที่ในใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="2a066-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="2a066-109">ธุรกรรมการประเมินค่าใหม่ถูกสร้างขึ้นโดยย้อนกลับการประเมินค่าใหม่ตามสกุลเงินต่างประเทศล่าสุด</span><span class="sxs-lookup"><span data-stu-id="2a066-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="2a066-110">ดังนั้น ธุรกรรมที่เปิดอยู่จะมีการประเมินค่าสกุลเงินทางบัญชีของต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="2a066-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="2a066-111">อัพเกรดเป็นรุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="2a066-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="2a066-112">เรียกใช้กระบวนการประเมินค่าตามสกุลเงินต่างประเทศสำหรับบัญชีเจ้าหนี้และบัญชีลูกหนี้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2a066-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="2a066-113">จากนั้น ตั้งค่าฟิลด์ **วิธีการ** เป็น **มาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="2a066-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="2a066-114">ธุรกรรมการประเมินค่าใหม่ถูกสร้างขึ้นโดยขึ้นอยู่กับอัตราแลกเปลี่ยนปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="2a066-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="2a066-115">ธุรกรรมนี้จะบันทึกกำไร/ขาดทุนที่เกิดขึ้นจริงและบัญชีแยกประเภทสรุปที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2a066-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]