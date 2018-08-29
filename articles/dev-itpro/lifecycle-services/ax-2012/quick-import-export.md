---
title: "นำเข้า-ส่งออกด่วน"
description: "วัตถุประสงค์ของการนำเข้าส่งออกด่วนคือเพื่อช่วยให้คุณสามารถนำเข้าและส่งออกโดยมีขั้นตอนที่น้อยลง"
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: AX 2012
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 4f2edba4add691e9ad4c7829551c6f79b9804853
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---

# <a name="quick-import-export"></a><span data-ttu-id="5e594-103">นำเข้า-ส่งออกด่วน</span><span class="sxs-lookup"><span data-stu-id="5e594-103">Quick import export</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5e594-104">วัตถุประสงค์ของการนำเข้าส่งออกด่วนคือเพื่อช่วยให้คุณสามารถนำเข้าและส่งออกโดยมีขั้นตอนที่น้อยลง</span><span class="sxs-lookup"><span data-stu-id="5e594-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="5e594-105">เราได้เพิ่มคุณลักษณะการนำเข้าส่งออกด่วนเพื่อให้ผู้ใช้สามารถนำเข้าหรือส่งออกงานอย่างง่ายที่พวกเขาต้องการดำเนินการอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="5e594-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="5e594-106">ตามหลักการคุณลักษณะนี้ควรถูกนำไปใช้ในสถานการณ์ที่ไฟล์แม็ปไปยังระบบโดยอัตโนมัติและผู้ใช้ไม่จำเป็นต้องทำการแม็ปขั้นสูง หรือสร้างงานนำเข้าหรือส่งออกซ้ำ</span><span class="sxs-lookup"><span data-stu-id="5e594-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

- <span data-ttu-id="5e594-107">คุณลักษณะนี้สนับสนุนการทำงานกับเอนทิตีแบบนอกกรอบและแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="5e594-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
- <span data-ttu-id="5e594-108">คุณสามารถนำเข้าจากแฟ้ม และถ้าคุณกำลังใช้แหล่งข้อมูล ODBC คุณสามารถเลือกแบบสอบถามเพื่อใช้ในการกำหนดการนำเข้าของคุณได้</span><span class="sxs-lookup"><span data-stu-id="5e594-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
- <span data-ttu-id="5e594-109">คุณจะต้องกำหนดรูปแบบของข้อมูลต้นทางสำหรับ AX หรือไฟล์ไว้แล้ว และทราบว่าเก็บไว้ที่ใด</span><span class="sxs-lookup"><span data-stu-id="5e594-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
- <span data-ttu-id="5e594-110">คุณไม่จำเป็นต้องสร้างกลุ่มการประมวลผลเพื่อใช้การนำเข้า/ส่งออกด่วน ระบบจะสร้างรายการหนึ่ง ๆ ขึ้นโดยอัตโนมัติเมื่อมีการดำเนินการนำเข้าหรือส่งออกงาน</span><span class="sxs-lookup"><span data-stu-id="5e594-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="5e594-111">คุณยังสามารถเลือกเก็บประวัติของข้อมูลที่นำเข้าโดยการนำเข้า/ส่งออกด่วนได้</span><span class="sxs-lookup"><span data-stu-id="5e594-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="5e594-112">โปรดทราบว่าการนำเข้าส่งออกด่วนจะถือว่าคุณคุ้นเคยกับแนวคิดของ DIXF</span><span class="sxs-lookup"><span data-stu-id="5e594-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>




