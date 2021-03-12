---
title: การโอนย้ายบัญชีแยกประเภทย่อยไปยังบัญชีแยกประเภททั่วไป
description: หัวข้อนี้จะอธิบายความสามารถใน Microsoft Dynamics 365 Finance ที่เกี่ยวข้องกับกระบวนการโอนย้ายบัญชีแยกประเภทย่อยในบัญชีแยกประเภททั่วไป
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: de9328f69938151c5558d41263d36b873d117e4b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975494"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="7814f-103">การโอนย้ายบัญชีแยกประเภทย่อยไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="7814f-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7814f-104">หัวข้อนี้จะอธิบายความสามารถใน Microsoft Dynamics 365 Finance ที่เกี่ยวข้องกับกฎสำหรับการโอนย้ายชุดงานของรายการสมุดรายวันบัญชีแยกประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="7814f-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="7814f-105">ในรุ่น 8.1 ได้ทำการเปลี่ยนแปลงเพื่ออนุญาตให้มีการโอนย้ายกฎ ซึ่งเลิกสนับสนุนตัวเลือก **ซิงโครนัส**</span><span class="sxs-lookup"><span data-stu-id="7814f-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="7814f-106">สำหรับข้อมูลเพิ่มเติม ให้ดู [คุณลักษณะที่ลบหรือถูกเลิกใช้สำหรับ Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20)</span><span class="sxs-lookup"><span data-stu-id="7814f-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="7814f-107">ตัวเลือกต่อไปนี้จะพร้อมใช้งานสำหรับการโอนย้ายชุดงานบัญชีแยกประเภทย่อย</span><span class="sxs-lookup"><span data-stu-id="7814f-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="7814f-108">แบบอะซิงโครนัส – ตัวเลือกนี้จะจัดกำหนดการโอนย้ายรายการบัญชีแยกประเภทย่อยไปยังบัญชีแยกประเภททั่วไปโดยทันที</span><span class="sxs-lookup"><span data-stu-id="7814f-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="7814f-109">จะมีการบันทึกใบสำคัญบัญชีแยกประเภททั่วไปทันทีที่ทรัพยากรพร้อมที่จะประมวลผลคำขอนี้บนเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="7814f-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="7814f-110">ชุดงานที่จัดกำหนดการ – ตัวเลือกนี้จะเพิ่มรายการบัญชีแยกประเภทย่อยที่มีการโอนย้ายไปยังคิวการประมวลผลในบัญชีแยกประเภททั่วไป ที่ซึ่งจะมีการประมวลผลรายการตามใบสั่งที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="7814f-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="7814f-111">จะมีการบันทึกใบสำคัญบัญชีแยกประเภททั่วไปในเวลาที่จัดกำหนดการ หากทรัพยากรพร้อมที่จะประมวลผลชุดงานนี้บนเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="7814f-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="7814f-112">ในรุ่น 10.0.8 มีการปรับปรุงเพื่อเพิ่มประสิทธิภาพการทำงานของตัวเลือกอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="7814f-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="7814f-113">คุณลักษณะนี้ถูกเปิดใช้งานภายใต้ชื่อคุณลักษณะ **การโอนย้ายบัญชีแยกประเภทย่อยไปยังการเพิ่มประสิทธิภาพบัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="7814f-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="7814f-114">ฟังก์ชันนี้ช่วยปรับปรุงการโอนย้ายข้อมูลจากบัญชีแยกประเภทย่อยไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="7814f-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="7814f-115">ซึ่งจะช่วยให้กระบวนการมีประสิทธิภาพมากขึ้น และจะจัดกลุ่มชุดของธุรกรรมที่มีขนาดเล็กลงเข้าด้วยกันเพื่อโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="7814f-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="7814f-116">การทำเช่นนี้ช่วยให้สามารถใช้เซิร์ฟเวอร์ชุดงานได้อย่างมีประสิทธิภาพมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="7814f-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="7814f-117">ฟังก์ชันนี้จำเป็นต้องมีการตั้งค่าเซิร์ฟเวอร์ชุดงานแบบออนไลน์และทำงานเพื่อให้ตัวเลือกการโอนย้ายอะซิงโครนัสทำงาน</span><span class="sxs-lookup"><span data-stu-id="7814f-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 
