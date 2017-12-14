---
title: "ภาพรวมของ Positive pay"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับ positive pay ซึ่งถูกใช้ในการสร้างรายการอิเล็กทรอนิกส์ของเช็คที่สามารถแสดงให้กับธนาคารได้"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: cb5a674472936a52b624c548fd37079d57eb6cb7
ms.openlocfilehash: 70e0249ccf317a5a59afd97899187ee58409de22
ms.contentlocale: th-th
ms.lasthandoff: 12/14/2017

---

# <a name="positive-pay-overview"></a><span data-ttu-id="f4e3b-103">ภาพรวมของ Positive pay</span><span class="sxs-lookup"><span data-stu-id="f4e3b-103">Positive pay overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f4e3b-104">บทความนี้แสดงข้อมูลเกี่ยวกับ positive pay ซึ่งถูกใช้ในการสร้างรายการอิเล็กทรอนิกส์ของเช็คที่สามารถแสดงให้กับธนาคารได้</span><span class="sxs-lookup"><span data-stu-id="f4e3b-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="f4e3b-105">Positive pay ถูกใช้ในการสร้างรายการอิเล็กทรอนิกส์ของเช็คที่สามารถแสดงให้กับธนาคาร </span><span class="sxs-lookup"><span data-stu-id="f4e3b-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="f4e3b-106">ไฟล์ Positive pay สามารถช่วยธนาคารป้องกันการฉ้อโกงเช็ค </span><span class="sxs-lookup"><span data-stu-id="f4e3b-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="f4e3b-107">คุณตั้งค่า Positive pay เพื่อสร้างรายการอิเล็กทรอนิกส์ของเช็คทุกครั้งที่มีการพิมพ์เช็ค </span><span class="sxs-lookup"><span data-stu-id="f4e3b-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="f4e3b-108">แล้วจากนั้นเมื่อมีการนำเสนอเช็คให้กับธนาคาร ธนาคารจะเปรียบเทียบเช็คกับรายการเช็คที่คุณส่งไปก่อนหน้านี้ </span><span class="sxs-lookup"><span data-stu-id="f4e3b-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="f4e3b-109">ถ้าเช็คตรงกับเช็คในรายการ ธนาคารจะเคลียร์เช็ค </span><span class="sxs-lookup"><span data-stu-id="f4e3b-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="f4e3b-110">ถ้าเช็คไม่ตรงกัน ธนาคารจะระงับเช็คไว้เพื่อตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="f4e3b-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="f4e3b-111">Positive pay ถูกเรียกอีกอย่างว่า SafePay </span><span class="sxs-lookup"><span data-stu-id="f4e3b-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="f4e3b-112">ไฟล์ positive pay สามารถประกอบด้วยข้อมูลที่สำคัญเกี่ยวกับผู้จ่าย และยอดเงินเช็ค </span><span class="sxs-lookup"><span data-stu-id="f4e3b-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="f4e3b-113">ดังนั้นตรวจสอบให้แน่ใจว่า คุณใช้มาตรการด้านความปลอดภัยที่เหมาะสมจากเวลาที่มีการสร้างไฟล์ จนกระทั่งได้รับโดยธนาคาร </span><span class="sxs-lookup"><span data-stu-id="f4e3b-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="f4e3b-114">ไฟล์ Positive pay จะถูกดาวน์โหลดตามคำแนะนำในการดาวน์โหลดสำหรับเว็บเบราเซอร์ </span><span class="sxs-lookup"><span data-stu-id="f4e3b-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="f4e3b-115">มีสร้างไฟล์ positive pay โดยการใช้เอนทิตีข้อมูล </span><span class="sxs-lookup"><span data-stu-id="f4e3b-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="f4e3b-116">ก่อนที่คุณสร้างไฟล์ Positive pay คุณต้องตั้งค่ารูปแบบของการแปลงสำหรับ XML ที่แปลข้อมูลเป็นรูปแบบที่ธนาคารสามารถใช้ได้ </span><span class="sxs-lookup"><span data-stu-id="f4e3b-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="f4e3b-117">สำหรับแต่ละบัญชีธนาคารที่คุณต้องการสร้างข้อมูล Positive pay ให้ คุณต้องกำหนดรูปแบบ Positive pay </span><span class="sxs-lookup"><span data-stu-id="f4e3b-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="f4e3b-118">หลังจากที่คุณได้สร้างการชำระเงิน คุณสามารถสร้างไฟ Positive pay สำหรับนิติบุคคลเดี่ยวและบัญชีธนาคารเดี่ยวได้ </span><span class="sxs-lookup"><span data-stu-id="f4e3b-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="f4e3b-119">อีกทางหนึ่งคือ คุณสามารถสร้างไฟล์ Positive pay สำหรับหลายนิติบุคคลและหลายบัญชีธนาคารในเวลาเดียวกันได้ </span><span class="sxs-lookup"><span data-stu-id="f4e3b-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="f4e3b-120">หลังจากที่เช็คที่ถูกรายการในไฟล์ positive pay ได้ถูกชำระ คุณจะได้รับหมายเลขการยืนยันจากธนาคารของคุณ </span><span class="sxs-lookup"><span data-stu-id="f4e3b-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="f4e3b-121">คุณจะได้รับหมายเลขการยืนยันจากธนาคารของคุณ จากนั้นคุณสามารถยืนยันไฟ Positive pay ใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ได้</span><span class="sxs-lookup"><span data-stu-id="f4e3b-121">You can then confirm the positive pay file in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> 

<span data-ttu-id="f4e3b-122">ถ้าคุณต้องเปลี่ยนไฟล์ positive pay คุณสามารถเรียกคืนได้ </span><span class="sxs-lookup"><span data-stu-id="f4e3b-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="f4e3b-123">จากนั้นสำหรับเช็คแต่ละรายการในไฟล์ Positive pay ฟิลด์ที่บ่งชี้ว่าเช็คได้ถูกรวมอยู่ในไฟล์ Positive pay หรือไม่ จะถูกรีเซ็ต</span><span class="sxs-lookup"><span data-stu-id="f4e3b-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="f4e3b-124">สำหรับข้อมูลเพิ่มเติม ดู [ตั้งค่าและสร้างไฟล์ Positive Pay](set-up-generate-positive-pay-files.md)</span><span class="sxs-lookup"><span data-stu-id="f4e3b-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>




