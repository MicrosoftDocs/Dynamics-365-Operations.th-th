---
title: โอนย้ายสินทรัพย์ถาวร
description: คู่มืองานนี้จะโอนข้อมูลทางการเงินสำหรับสมุดบัญชีสินทรัพย์ถาวรจากหนึ่งชุดมิติทางการเงินเพื่อตั้งค่ามิติทางการเงินใหม่
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8a5b94d9a0bb510daa2a698524e0c380597991
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "357208"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="70e69-103">โอนย้ายสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="70e69-103">Transfer a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70e69-104">คู่มืองานนี้จะโอนข้อมูลทางการเงินสำหรับสมุดบัญชีสินทรัพย์ถาวรจากหนึ่งชุดมิติทางการเงินเพื่อตั้งค่ามิติทางการเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="70e69-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="70e69-105">ใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="70e69-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="70e69-106">ไปที่ สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="70e69-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="70e69-107">ในรายการ ค้นหาและเลือกสินทรัพย์ถาวรที่จะโอน</span><span class="sxs-lookup"><span data-stu-id="70e69-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="70e69-108">ในบานหน้าต่างการดำเนินการ คลิกสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="70e69-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="70e69-109">คลิกโอนสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="70e69-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="70e69-110">ในฟิลด์วันที่การโอน ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="70e69-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="70e69-111">ป้อนข้อคิดเห็นที่อธิบายการโอน</span><span class="sxs-lookup"><span data-stu-id="70e69-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="70e69-112">รายการนี้แสดงสมุดบัญชีทั้งหมดสำหรับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="70e69-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="70e69-113">ทำเครื่องหมายสมุดบัญชีที่คุณต้องการโอนไปยังชุดมิติทางการเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="70e69-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="70e69-114">รายการนี้แสดงค่ามิติทางการเงินที่มีอยู่สำหรับสมุดบัญชีที่เลือก</span><span class="sxs-lookup"><span data-stu-id="70e69-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="70e69-115">เลือกมิติทางการเงินที่คุณต้องการอัพเดตสำหรับสมุดบัญชีสินทรัพย์ถาวรที่เลือก</span><span class="sxs-lookup"><span data-stu-id="70e69-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="70e69-116">ในฟิลด์มิติทางการเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="70e69-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="70e69-117">ตั้งค่ามิติทางการเงินอื่นๆ ตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="70e69-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="70e69-118">ทุกค่ามิติทางการเงินจะเปลี่ยนไปเมื่อมีการโอนเกิดขึ้น ไม่ว่าจะเป็นค่าที่ได้รับการป้อนหรือเว้นว่าง </span><span class="sxs-lookup"><span data-stu-id="70e69-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="70e69-119">ในตัวอย่าง ถ้าคุณป้อนค่าสำหรับหน่วยธุรกิจและปล่อยศูนย์ต้นทุนและแผนกมิติทางการเงินให้ว่างไว้</span><span class="sxs-lookup"><span data-stu-id="70e69-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="70e69-120">ถ้าโครงสร้างทางบัญชีของคุณอนุญาตให้มีค่าว่างเปล่าสำหรับศูนย์ต้นทุนและแผนก การโอนจะส่งผลให้แต่ละรูปแบบมูลค่ามีค่าใหม่สำหรับหน่วยธุรกิจและค่าว่างสำหรับศูนย์ต้นทุนและแผนก</span><span class="sxs-lookup"><span data-stu-id="70e69-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="70e69-121">คลิก อัพเดต ข้อมูลเพิ่มเติมจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="70e69-121">Click Update.</span></span>
    * <span data-ttu-id="70e69-122">คุณมีโอกาสที่จะแสดงตัวอย่างการเปลี่ยนแปลงก่อนที่จะเสร็จสิ้นการโอน</span><span class="sxs-lookup"><span data-stu-id="70e69-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="70e69-123">ตรวจทานผลลัพธ์ก่อนที่จะมีการโอนสมุดบัญชีสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="70e69-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="70e69-124">คลิก โอนย้าย </span><span class="sxs-lookup"><span data-stu-id="70e69-124">Click Transfer.</span></span>

