---
title: เครื่องมือแก้ไขสูตรการรายงานทางอิเล็กทรอนิกส์ขั้นสูง
description: หัวข้อนี้อธิบายวิธีการใช้ตัวแก้ไขสูตรขั้นสูงเพื่อกำหนดค่านิพจน์ในการแม็ปโมเดลการรายงานทางอิเล็กทรอนิกส์ (ER) กับส่วนประกอบรูปแบบ
author: NickSelin
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 14eb8a59b64a49649768f93befdf8e6e8dcf8105
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685394"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="02e9f-103">เครื่องมือแก้ไขสูตรการรายงานทางอิเล็กทรอนิกส์ขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="02e9f-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02e9f-104">นอกจากนี้ [การรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md) [ตัวแก้ไขสูตร](general-electronic-reporting-formula-designer.md) คุณสามารถใช้ตัวแก้ไขสูตรการรายงานทางอิเล็กทรอนิกส์ขั้นสูงเพื่อปรับปรุงประสบการณ์ของการกำหนดค่านิพจน์การรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="02e9f-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="02e9f-105">ตัวแก้ไขขั้นสูงใช้เบราว์เซอร์และดำเนินการโดย [ตัวแก้ไข Monaco](https://microsoft.github.io/monaco-editor)</span><span class="sxs-lookup"><span data-stu-id="02e9f-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="02e9f-106">คุณลักษณะตัวแก้ไขขั้นสูงที่ใช้บ่อยที่สุดมีการอธิบายไว้ในหัวข้อนี้:</span><span class="sxs-lookup"><span data-stu-id="02e9f-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="02e9f-107">การจัดรูปแบบอัตโนมัติของรหัส</span><span class="sxs-lookup"><span data-stu-id="02e9f-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="02e9f-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="02e9f-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="02e9f-109">การทำรหัสให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="02e9f-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="02e9f-110">การนำทางรหัส</span><span class="sxs-lookup"><span data-stu-id="02e9f-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="02e9f-111">กำหนดโครงสร้างรหัส</span><span class="sxs-lookup"><span data-stu-id="02e9f-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="02e9f-112">ค้นหาและแทนที่</span><span class="sxs-lookup"><span data-stu-id="02e9f-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="02e9f-113">การวางข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02e9f-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="02e9f-114">การทำสีที่ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="02e9f-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="02e9f-115"><a name="ActivateAdvEditor">เริ่มการใช้งานตัวแก้ไขสูตรขั้นสูง</a></span><span class="sxs-lookup"><span data-stu-id="02e9f-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="02e9f-116">ทำตามขั้นตอนต่อไปนี้เพื่อเริ่มใช้ตัวแก้ไขสูตรขั้นสูงในอินสแตนซ์ Microsoft Dynamics 365 Finance ของคุณ</span><span class="sxs-lookup"><span data-stu-id="02e9f-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="02e9f-117">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="02e9f-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="02e9f-118">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="02e9f-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="02e9f-119">กล่องโต้ตอบ **พารามิเตอร์ผู้ใช้** ในส่วน **การติดตามการดำเนินการ** ตั้งค่าพารามิเตอร์ **ตัวแก้ไขสูตรขั้นสูง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="02e9f-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="02e9f-120">[![หน้าการตั้งค่าคอนฟิก ER](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="02e9f-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="02e9f-121">พึงระวังว่าพารามิเตอร์นี้เฉพาะผู้ใช้และเฉพาะบริษัท</span><span class="sxs-lookup"><span data-stu-id="02e9f-121">Be aware that this parameter is user specific and company specific.</span></span>

## <a name=""></a><span data-ttu-id="02e9f-122"><a name="Autoformatting">การจัดรูปแบบอัตโนมัติของรหัส</a></span><span class="sxs-lookup"><span data-stu-id="02e9f-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="02e9f-123">เมื่อคุณเขียนนิพจน์ที่ซับซ้อนที่ประกอบด้วยรหัสหลายแถว การเยื้องของบรรทัดที่ป้อนใหม่จะเป็นไปโดยอัตโนมัติตามการเยื้องของแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="02e9f-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="02e9f-124">คุณสามารถเลือกบรรทัดและเปลี่ยนการเยื้องได้โดยพิมพ์ **Tab** หรือ **Shift+Tab**.</span><span class="sxs-lookup"><span data-stu-id="02e9f-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="02e9f-125">[![ตัวแก้ไขสูตร ER](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="02e9f-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="02e9f-126">การจัดรูปแบบอัตโนมัติช่วยให้คุณสามารถรักษานิพจน์ทั้งหมดให้อยู่ในรูปแบบที่ดีเพื่อให้การบำรุงรักษาง่ายขึ้นและทำให้เข้าใจตรรกะที่กำหนดค่าได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="02e9f-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="02e9f-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="02e9f-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="02e9f-128">ตัวแก้ไขสนับสนุนการกรอกคำให้เสร็จสมบูรณ์เพื่อช่วยให้คุณเขียนนิพจน์ได้เร็วขึ้นและหลีกเลี่ยงการพิมพ์ผิด</span><span class="sxs-lookup"><span data-stu-id="02e9f-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="02e9f-129">เมื่อคุณเริ่มเพิ่มข้อความใหม่ ตัวแก้ไขนำเสนอรายการฟังก์ชันที่สนับสนุนในฟังก์ชัน ER โดยอัตโนมัติซึ่งมีอักขระที่คุณได้ป้อนไว้</span><span class="sxs-lookup"><span data-stu-id="02e9f-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="02e9f-130">คุณยังสามารถแสดงทริกเกอร์ IntelliSense ในสถานที่ใด ๆ ของนิพจน์ที่กำหนดค่าไว้โดยการพิมพ์ **Ctrl+Space**</span><span class="sxs-lookup"><span data-stu-id="02e9f-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="02e9f-131">[![ตัวแก้ไขสูตร ER](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="02e9f-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="02e9f-132"><a name="CodeCompletion">การทำรหัสให้เสร็จสมบูรณ์</a></span><span class="sxs-lookup"><span data-stu-id="02e9f-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="02e9f-133">ตัวแก้ไขจัดเตรียมการกรอกรหัสให้สมบูรณ์โดยอัตโนมัติโดย:</span><span class="sxs-lookup"><span data-stu-id="02e9f-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="02e9f-134">การแทรกวงเล็บปิดเมื่อป้อนวงเล็บเปิดไว้ และทำให้เคอร์เซอร์อยู่ในเครื่องหมายวงเล็บ</span><span class="sxs-lookup"><span data-stu-id="02e9f-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="02e9f-135">การแทรกสัญลักษณ์คำพูดที่สองเมื่อป้อนตัวแรก และทำให้เคอร์เซอร์อยู่ในเครื่องหมายคำพูด</span><span class="sxs-lookup"><span data-stu-id="02e9f-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="02e9f-136">การแทรกสัญลักษณ์คำพูดคู่ที่สองเมื่อป้อนตัวแรก และทำให้เคอร์เซอร์อยู่ในเครื่องหมายคำพูด</span><span class="sxs-lookup"><span data-stu-id="02e9f-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="02e9f-137">[![ตัวแก้ไขสูตร ER](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="02e9f-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="02e9f-138">เมื่อคุณชี้ไปที่วงเล็บที่พิมพ์แล้ว วงเล็บที่สองของคู่นี้จะถูกเน้นโดยอัตโนมัติเพื่อแสดงโครงสร้างที่รองรับ</span><span class="sxs-lookup"><span data-stu-id="02e9f-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="02e9f-139"><a name="CodeNavigation">การนำทางรหัส</a></span><span class="sxs-lookup"><span data-stu-id="02e9f-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="02e9f-140">คุณสามารถค้นหาตำแหน่งสัญลักษณ์หรือบรรทัดที่ต้องการในนิพจน์ของคุณโดยพิมพ์คำสั่ง **ไปยัง** โดยใช้ชุดคำสั่งหรือเมนูบริบท</span><span class="sxs-lookup"><span data-stu-id="02e9f-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="02e9f-141">ตัวอย่างเช่น เพื่อข้ามไปยังบรรทัด **8** กระทำได้ดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="02e9f-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="02e9f-142">กด **Ctrl+G** ป้อนค่า **8** แล้วกด **ป้อน**</span><span class="sxs-lookup"><span data-stu-id="02e9f-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="02e9f-143">หรือ</span><span class="sxs-lookup"><span data-stu-id="02e9f-143">-or-</span></span>

- <span data-ttu-id="02e9f-144">กด **F1** พิมพ์ **G** เลือก **ไปยังบรรทัด** ป้อนค่า **8** แล้วกด **ป้อน**</span><span class="sxs-lookup"><span data-stu-id="02e9f-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="02e9f-145">[![ตัวแก้ไขสูตร ER](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="02e9f-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="02e9f-146"><a name="CodeStructuring">กำหนดโครงสร้างรหัส</a></span><span class="sxs-lookup"><span data-stu-id="02e9f-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="02e9f-147">รหัสสำหรับฟังก์ชั่นบางอย่าง เช่น [IF](er-functions-logical-if.md) หรือ [CASE](er-functions-logical-case.md) จะถูกจัดโครงสร้างโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="02e9f-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="02e9f-148">คุณสามารถขยายและยุบขอบเขตที่ซ่อนอยู่ใด ๆ หรือทั้งหมดของรหัสนี้เพื่อลดส่วนที่แก้ไขได้ของนิพจน์ เพื่อเน้นเฉพาะชิ้นส่วนของรหัสที่คุณต้องให้ความสนใจ</span><span class="sxs-lookup"><span data-stu-id="02e9f-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="02e9f-149">คำสั่งสลับซ่อน/แสดง สามารถใช้สำหรับสิ่งนั้นได้</span><span class="sxs-lookup"><span data-stu-id="02e9f-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="02e9f-150">ตัวอย่างเช่น ซ่อนทุกภูมิภาค กระทำได้ดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="02e9f-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="02e9f-151">กด **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="02e9f-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="02e9f-152">หรือ</span><span class="sxs-lookup"><span data-stu-id="02e9f-152">-or-</span></span>

- <span data-ttu-id="02e9f-153">กด **F1** กด **FO** เลือก **ซ่อนทั้งหมด** แล้วจึงกด **ป้อน**</span><span class="sxs-lookup"><span data-stu-id="02e9f-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="02e9f-154">หากต้องการแสดงทุกภูมิภาค ให้ทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="02e9f-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="02e9f-155">กด **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="02e9f-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="02e9f-156">หรือ</span><span class="sxs-lookup"><span data-stu-id="02e9f-156">-or-</span></span>
  
- <span data-ttu-id="02e9f-157">กด **F1** พิมพ์ **UN** เลือก **แสดงทั้งหมด** แล้วจึงกด **ป้อน**</span><span class="sxs-lookup"><span data-stu-id="02e9f-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="02e9f-158">[![ตัวแก้ไขสูตร ER](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="02e9f-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="02e9f-159"><a name="FindAndReplace">ค้นหาและแทนที่</a></span><span class="sxs-lookup"><span data-stu-id="02e9f-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="02e9f-160">หากต้องการค้นหาข้อความบางข้อความ ให้เลือกข้อความในนิพจน์ของคุณ แล้วทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="02e9f-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="02e9f-161">กด **Ctrl+F** แล้วจึงกด **F3** เพื่อค้นหาข้อความที่ปรากฎขึ้นให้เลือกต่อไป หรือกด **Shift+F3** เพื่อค้นหาการเกิดขึ้นก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="02e9f-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="02e9f-162">หรือ</span><span class="sxs-lookup"><span data-stu-id="02e9f-162">-or-</span></span>
  
- <span data-ttu-id="02e9f-163">กด **F1** พิมพ์ **F** จากนั้นเลือกตัวเลือกที่ต้องการเพื่อค้นหาข้อความที่เลือก</span><span class="sxs-lookup"><span data-stu-id="02e9f-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="02e9f-164">เพื่อแทนที่ข้อความที่เกิดขึ้นบางข้อความ ให้เลือกข้อความในนิพจน์ของคุณ แล้วทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="02e9f-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="02e9f-165">กด **Ctrl+H**</span><span class="sxs-lookup"><span data-stu-id="02e9f-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="02e9f-166">ป้อนข้อความสำรองและเลือกตัวเลือกการแทนที่ เพื่อแทนที่ข้อความที่เลือกหรือข้อความทั้งหมดที่เกิดขึ้นในนิพจน์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="02e9f-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="02e9f-167">หรือ</span><span class="sxs-lookup"><span data-stu-id="02e9f-167">-or-</span></span>
  
- <span data-ttu-id="02e9f-168">กด **F1** พิมพ์ **R** จากนั้นเลือกตัวเลือกที่ต้องการเพื่อแทนที่ข้อความที่เลือก</span><span class="sxs-lookup"><span data-stu-id="02e9f-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="02e9f-169">ป้อนข้อความสำรองและเลือกตัวเลือกการแทนที่ เพื่อแทนที่ข้อความที่เลือกหรือข้อความทั้งหมดที่เกิดขึ้นในนิพจน์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="02e9f-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="02e9f-170">เพื่อเปลี่ยนข้อความที่เกิดขึ้นบางข้อความ ให้เลือกข้อความในนิพจน์ของคุณ แล้วทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="02e9f-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="02e9f-171">กด **Ctrl+F2** จากนั้นป้อนข้อความแสดงแทน</span><span class="sxs-lookup"><span data-stu-id="02e9f-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="02e9f-172">หรือ</span><span class="sxs-lookup"><span data-stu-id="02e9f-172">-or-</span></span>
  
- <span data-ttu-id="02e9f-173">กด **F1** พิมพ์ **C** จากนั้นเลือกตัวเลือกที่ต้องการเพื่อเปลี่ยนข้อความที่เลือก</span><span class="sxs-lookup"><span data-stu-id="02e9f-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="02e9f-174">ป้อนข้อความแสดงแทน</span><span class="sxs-lookup"><span data-stu-id="02e9f-174">Enter the alternative text.</span></span>

<span data-ttu-id="02e9f-175">[![ตัวแก้ไขสูตร ER](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="02e9f-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="02e9f-176"><a name="DataPasting">การวางแหล่งข้อมูลและฟังก์ชั่น</a></span><span class="sxs-lookup"><span data-stu-id="02e9f-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="02e9f-177">คุณสามารถเลือก **เพิ่มแหล่งข้อมูล** ซึ่งวางไปที่นิพจน์ปัจจุบันซึ่งเป็นแหล่งข้อมูลที่เลือกไว้ในปัจจุบันบนแผงด้านซ้าย **แหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="02e9f-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="02e9f-178">ในทางเดียวกัน คุณสามารถเลือก **เพิ่มฟังก์ชัน** ซึ่งวางไปที่นิพจน์ปัจจุบันซึ่งเป็นฟังก์ชันที่เลือกไว้ในปัจจุบันบนแผงด้านขวา **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="02e9f-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="02e9f-179">หากคุณใช้ตัวแก้ไขสูตร ER ฟังก์ชันที่เลือกหรือแหล่งข้อมูลที่เลือกจะถูกวางไว้ที่ส่วนท้ายของนิพจน์ที่กำหนดค่าไว้เสมอ</span><span class="sxs-lookup"><span data-stu-id="02e9f-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="02e9f-180">เมื่อคุณใช้ตัวแก้ไขสูตร ER ขั้นสูง ฟังก์ชันที่เลือกหรือแหล่งข้อมูลที่เลือกจะสามารถวางไว้ที่ส่วนใดส่วนหนึ่งของนิพจน์ที่กำหนดค่าไว้ได้</span><span class="sxs-lookup"><span data-stu-id="02e9f-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="02e9f-181">คุณจะต้องใช้เคอร์เซอร์เพื่อระบุตำแหน่งที่คุณต้องการวางข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02e9f-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="02e9f-182">[![ตัวแก้ไขสูตร ER](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="02e9f-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="02e9f-183"><a name="SyntaxColorization">การทำสีที่ไวยากรณ์</a></span><span class="sxs-lookup"><span data-stu-id="02e9f-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="02e9f-184">ขณะนี้มีการใช้สีที่แตกต่างกันเพื่อเน้นส่วนต่างๆของนิพจน์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="02e9f-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="02e9f-185">ข้อความในเครื่องหมายวงเล็บคู่ที่สามารถแสดงป้ายชื่อรหัสของค่าคงที่ข้อความ</span><span class="sxs-lookup"><span data-stu-id="02e9f-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="02e9f-186">[![ตัวแก้ไขสูตร ER](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="02e9f-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="02e9f-187">การจำกัด</span><span class="sxs-lookup"><span data-stu-id="02e9f-187">Limitations</span></span>

<span data-ttu-id="02e9f-188">ขณะนี้โปรแกรมแก้ไขได้รับการสนับสนุนในเว็บเบราเซอร์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="02e9f-188">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="02e9f-189">Chrome</span><span class="sxs-lookup"><span data-stu-id="02e9f-189">Chrome</span></span>
- <span data-ttu-id="02e9f-190">Edge</span><span class="sxs-lookup"><span data-stu-id="02e9f-190">Edge</span></span>
- <span data-ttu-id="02e9f-191">Firefox</span><span class="sxs-lookup"><span data-stu-id="02e9f-191">Firefox</span></span>
- <span data-ttu-id="02e9f-192">Opera</span><span class="sxs-lookup"><span data-stu-id="02e9f-192">Opera</span></span>
- <span data-ttu-id="02e9f-193">Safari</span><span class="sxs-lookup"><span data-stu-id="02e9f-193">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="02e9f-194">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="02e9f-194">Additional resources</span></span>

- [<span data-ttu-id="02e9f-195">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="02e9f-195">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="02e9f-196">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="02e9f-196">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="02e9f-197">ตัวแก้ไข Monaco</span><span class="sxs-lookup"><span data-stu-id="02e9f-197">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)
