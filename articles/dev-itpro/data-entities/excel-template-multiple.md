---
title: "นำเข้าข้อมูลจากเท็มเพลตเอนทิตีข้อมูล Excel ที่มีแผ่นงานหลายแผ่น"
description: "หัวข้อนี้อธิบายวิธีการนำเข้าข้อมูลโดยใช้เท็มเพลตเอนทิตี้ข้อมูล Excel ไปยัง Microsoft Dynamics 365 for Finance and Operations, Enterprise edition"
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: b314a649829dd14a525923802e19b847dc5a115e
ms.contentlocale: th-th
ms.lasthandoff: 02/27/2018

---

# <a name="excel-templates-with-multiple-worksheets"></a><span data-ttu-id="4ba78-103">เท็มเพลต Excel ที่มีแผ่นงานหลายแผ่น</span><span class="sxs-lookup"><span data-stu-id="4ba78-103">Excel templates with multiple worksheets</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4ba78-104">การจัดการข้อมูลใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition สนับสนุนเท็มเพลตตาม Microsoft Excel สำหรับเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4ba78-104">Data management in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="4ba78-105">เท็มเพลตเหล่านี้ประกอบด้วยแผ่นงานอย่างน้อยหนึ่งแผ่น</span><span class="sxs-lookup"><span data-stu-id="4ba78-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="4ba78-106">เท็มเพลตที่มีแผ่นงานหลายแผ่นมักถูกใช้ เมื่อสะดวกในการจัดการข้อมูลในแฟ้มเดียว และในการนำเข้าไปยังเอนทิตีข้อมูลหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="4ba78-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="4ba78-107">ตัวอย่างอาจเป็นไซต์และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ba78-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="4ba78-108">อัพโหลดไฟล์ครั้งเดียว และแม็ปกับเอนทิตีทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4ba78-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="4ba78-109">ลองดูตัวอย่างที่มีไฟล์ Excel หนึ่งไฟล์ซึ่งมีแผ่นงานที่เรียกว่า **ไซต์** และ **คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4ba78-109">Let’s take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="4ba78-110">ในการตั้งค่าโครงการนำเข้าข้อมูล คุณก็จะสามารถเพิ่มเอนทิตี้ข้อมูลแรก **ไซต์** แล้วจากนั้น อัพโหลดไฟล์</span><span class="sxs-lookup"><span data-stu-id="4ba78-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="4ba78-111">คุณจะสามารถเลือก **ไซต์** เป็นแผ่นงานที่จะใช้สำหรับเอนทิตี้นี้ได้</span><span class="sxs-lookup"><span data-stu-id="4ba78-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="4ba78-112">ถ้าคุณเพิ่มเอนทิตี้ที่สอง **คลังสินค้า** โดยไม่ออกจากฟอร์ม **เพิ่มไฟล์** การค้นหาแผ่นงานจะช่วยให้คุณสามารถเลือกแผ่นงาน **คลังสินค้า** ได้ โดยไม่ต้องอัพโหลดไฟล์อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="4ba78-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="4ba78-113">เหตุผลเดียวในการอัพโหลดไฟล์ใหม่คือ ถ้าข้อมูล **คลังสินค้า** อยู่ในไฟล์อื่น</span><span class="sxs-lookup"><span data-stu-id="4ba78-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![แผ่นงานหลายแผ่น](./media/AddFileMultipleWorkSheets.png) 

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="4ba78-115">กำหนดแผ่นงานให้การแม็ปเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="4ba78-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="4ba78-116">คุณสามารถกำหนดการแม็ปของแผ่นงานให้กับเอนทิตีข้อมูลในงานการนำเข้าจากกริดได้</span><span class="sxs-lookup"><span data-stu-id="4ba78-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="4ba78-117">คอลัมน์ **แผ่นงาน** ในกริด แสดงแผ่นงานจากไฟล์ที่ถูกแม็ป</span><span class="sxs-lookup"><span data-stu-id="4ba78-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="4ba78-118">คุณสามารถเลือกแผ่นงานอื่นจากเมนูแบบหล่นลงได้</span><span class="sxs-lookup"><span data-stu-id="4ba78-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="4ba78-119">ถ้ามีการแม็ปแผ่นงานที่เลือกไปยังเอนทิตี้ในโครงการข้อมูล ระบบจะขอให้คุณยืนยันการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="4ba78-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="4ba78-120">เราขอแนะนำให้ คุณแก้ไขการแม็ปทั้งหมดในกริด</span><span class="sxs-lookup"><span data-stu-id="4ba78-120">We recommend that you fix all mappings in the grid.</span></span>

![อัพเดตการแม็ปแผ่นงาน](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="4ba78-122">แม็ปไปยังแฟ้มใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="4ba78-122">Re-map to a new file</span></span>

<span data-ttu-id="4ba78-123">ในกรณีที่ต้องอัพโหลดเป็นเวอร์ชันใหม่ของไฟล์เดียวกันหรือไฟล์ใหม่ทั้งหมด สำหรับเอนทิตี้ที่มีอยู่ในโครงการข้อมูล คุณต้องใช้อัพเดต **เพิ่มไฟล์** แล้วเพิ่มเอนทิตีอีกครั้ง ราวกับว่ามีการเพิ่มเป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="4ba78-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="4ba78-124">ระบบจะยืนยันว่า คุณต้องการเขียนทับเอนทิตี้ที่มีอยู่ในโครงการข้อมูลก่อนดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="4ba78-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="4ba78-125">เอนทิตีที่ไม่ได้ถูกเพิ่มอีกครั้ง (หรือถูกเขียนทับ) จะยึดการแม็ปก่อนหน้าจากไฟล์ก่อนหน้านี้ต่อไป</span><span class="sxs-lookup"><span data-stu-id="4ba78-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="4ba78-126">อัพโหลดไฟล์โดยใช้ รันโครงการ</span><span class="sxs-lookup"><span data-stu-id="4ba78-126">Upload a file using Run project</span></span>

<span data-ttu-id="4ba78-127">คุณสามารถอัปโหลดไฟล์ Excel ได้ในขณะที่ใช้ตัวเลือก **รันโครงการ** เพื่อดำเนินการโครงการที่นำเข้าได้</span><span class="sxs-lookup"><span data-stu-id="4ba78-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="4ba78-128">คุณต้องระมัดระวังในการอัพโหลดเฉพาะไฟล์ที่มีแผ่นงานเหมือนกับการแม็ปที่มีอยู่ในเอนทิตี้ข้อมูลในโครงการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4ba78-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="4ba78-129">ถ้าไม่พบแผ่นงานในไฟล์ที่เพิ่งอัพโหลด ระบบจะแสดงข้อผิดพลาด และจะหยุดการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="4ba78-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="4ba78-130">ถ้าต้องเปลี่ยนการแม็ปไปยังแผ่นงานสำหรับเอนทิตี้ การแม็ปในโครงการข้อมูลจึงต้องมีการอัพเดตจากภายในโครงการข้อมูลเป็นอันดับแรก ก่อนที่จะใช้ไฟล์ในประสบการณ์ **รันโครงการ**</span><span class="sxs-lookup"><span data-stu-id="4ba78-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>


