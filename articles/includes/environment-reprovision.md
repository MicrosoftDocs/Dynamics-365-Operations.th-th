<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="environment-reprovision.md" target-language="th-TH">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>environment-reprovision.33170a.795ff0c91f6e5c2ac83dd610a125d2f6fdbbec70.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>795ff0c91f6e5c2ac83dd610a125d2f6fdbbec70</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\includes\environment-reprovision.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101">
          <source>When copying a database between environments, you will need to run the environment re-provisioning tool before the copied database is fully functional, to ensure that all Retail components are up-to-date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อคัดลอกฐานข้อมูลระหว่างสภาพแวดล้อม คุณจะต้องรันเครื่องมือการเตรียมใช้งานใหม่สำหรับสภาพแวดล้อม ก่อนที่ฐานข้อมูลที่คัดลอกไว้จะใช้งานได้อย่างเต็มความสามารถ เพื่อให้แน่ใจว่าส่วนประกอบของ Retail ทั้งหมดมีความทันสมัย</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102">
          <source>We recommend that you run this procedure whether you are using Retail components or not, because Retail functionality is included in all environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เราแนะนำให้คุณรันกระบวนงานนี้ไม่ว่าคุณจะใช้ส่วนประกอบของ Retail อยู่หรือไม่ เนื่องจากมีการรวมฟังก์ชันของ Retail ไว้ในทุกสภาพแวดล้อม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Before you continue, you must make sure that the following prerequisites are met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ก่อนที่คุณจะดำเนินการต่อ คุณต้องแน่ใจว่าได้ทำตามข้อกำหนดเบื้องต้นดังต่อไปนี้:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>If you are upgrading to the July 2017 release (also known as 7.2) 7.2.11792.56024, apply the following application X++ hotfixes in the destination environment before running the data upgrade in that environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หากคุณกำลังจะอัพเกรดเป็นรุ่นที่นำออกใช้เดือนกรกฎาคม 2017 (หรือเรียกอีกอย่างหนึ่งว่า 7.2) 7.2.11792.56024 ให้ใช้โปรแกรมแก้ไขด่วน X++ สำหรับแอพลิเคชันต่อไปนี้ในสภาพแวดล้อมปลายทางก่อนที่จะรันการอัพเกรดข้อมูลในสภาพแวดล้อมดังกล่าว</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>These will prevent various errors occurring during the data upgrade:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">วิธีนี้จะช่วยป้องกันข้อผิดพลาดต่างๆ ที่เกิดขึ้นในระหว่างการอัพเกรดข้อมูล:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>KB 4036156 - Retail minor version upgrade - 'Variant number sequence is not set.'</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4036156 - การอัพเกรดเวอร์ชันรองของ Retail - "ไม่ได้ตั้งค่าลำดับหมายเลขของตัวแปร"</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This fix package also includes KB 4035399 and KB 4035751.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">แพคเกจการแก้ไขนี้ยังประกอบด้วย KB 4035399 และ KB 4035751</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Note that you must have a minimum of Platform Update 9 to use this package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">โปรดทราบว่าคุณต้องมี Platform Update 9 เป็นอย่างต่ำจึงจะใช้แพคเกจนี้ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>If you are unsure, install the latest binaries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หากคุณไม่แน่ใจ ให้ติดตั้งไบนารีล่าสุด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If you are upgrading from Microsoft Dynamics AX 2012, install the following application X++ fixes in the destination environment before you run the data upgrade:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หากคุณกำลังอัพเกรดจาก Microsoft Dynamics AX 2012 ให้ติดตั้งโปรแกรมแก้ไข X++ สำหรับแอพลิเคชันต่อไปนี้ในสภาพแวดล้อมปลายทางก่อนที่คุณจะรันการอัพเกรดข้อมูล:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>KB 4033183 - Dynamics AX 2012 R2 or Dynamics AX 2012 R3 Pre-CU8 non-retail upgrade fails with Object not found for dbo.RETAILTILLLAYOUTZONE.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4033183 - Dynamics AX 2012 R2 หรือ Dynamics AX 2012 R3 Pre-CU8 การอัพเกรดที่ไม่ใช่การขายปลีกจะล้มเหลวและไม่พบออบเจกต์สำหรับ dbo.RETAILTILLLAYOUTZONE</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>KB 4040692 - Dynamics AX 2012 R3 to Microsoft Dynamics 365 for Operations 7.2 upgrade fails on RetailSalesLine duplicate index on SalesLineIdx.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4040692 - การอัพเกรด Dynamics AX 2012 R3 เป็น Microsoft Dynamics 365 for Operations 7.2 ล้มเหลวในดัชนีที่ซ้ำกัน RetailSalesLine ใน SalesLineIdx</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>KB 4035490 - Performance issue with GeneralJournalAccountEntry MainAccount field upgrade script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4035490 - ปัญหาประสิทธิภาพการทำงานที่มีสคริปต์การอัพเกรดฟิลด์ GeneralJournalAccountEntry MainAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Follow these steps to run the Environment reprovisioning tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ทำตามขั้นตอนเหล่านี้เพื่อรันเครื่องมือการเตรียมใช้งานใหม่สภาพแวดล้อม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In the Shared asset library, select <bpt id="p1">**</bpt>Software deployable package<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในไลบรารีสินทรัพย์ที่ใช้ร่วมกัน เลือก <bpt id="p1">**</bpt>แพคเกจที่สามารถปรับใช้ได้ของซอฟต์แวร์<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Download the Environment reprovisioning tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ดาวน์โหลดเครื่องมือการเตรียมใช้งานใหม่สภาพแวดล้อม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the asset library for your project, select <bpt id="p1">**</bpt>Software deployable package<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในไลบรารีสินทรัพย์สำหรับโครงการของคุณ เลือก <bpt id="p1">**</bpt>แพคเกจที่สามารถปรับใช้ได้ของซอฟต์แวร์<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Select <bpt id="p1">**</bpt>New<ept id="p1">**</ept> to create a new package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เลือก <bpt id="p1">**</bpt>สร้าง<ept id="p1">**</ept> เพื่อสร้างแพคเกจใหม่</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Enter a name and description for the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ป้อนชื่อและคำอธิบายสำหรับแพจเกจ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You can use <bpt id="p1">**</bpt>Environment reprovisioning tool<ept id="p1">**</ept> as the package name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณสามารถใช้ <bpt id="p1">**</bpt>เครื่องมือการเตรียมใช้งานใหม่สภาพแวดล้อม<ept id="p1">**</ept> เป็นชื่อแพคเกจ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Upload the package that you downloaded earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อัพโหลดแพคเกจที่คุณดาวน์โหลดไว้ก่อนหน้านี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>On the <bpt id="p1">**</bpt>Environment details<ept id="p1">**</ept> page for your target environment, select <bpt id="p2">**</bpt>Maintain<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Apply updates<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในหน้า <bpt id="p1">**</bpt>รายละเอียดสภาพแวดล้อม<ept id="p1">**</ept> สำหรับสภาพแวดล้อมเป้าหมายของคุณ เลือก <bpt id="p2">**</bpt>รักษา<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>ใช้การอัพเดต<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Select the Environment reprovisioning tool that you uploaded earlier, and then select <bpt id="p1">**</bpt>Apply<ept id="p1">**</ept> to apply the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เลือกเครื่องมือการเตรียมใช้งานใหม่สภาพแวดล้อมที่คุณอัพโหลดไว้ก่อนหน้านี้ จากนั้นเลือก <bpt id="p1">**</bpt>ใช้<ept id="p1">**</ept> เพื่อใช้แพคเกจ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Monitor the progress of the package deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตรวจสอบความคืบหน้าในการปรับใช้แพคเกจ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For more information about how to apply a deployable package, see <bpt id="p1">[</bpt>Apply a deployable package<ept id="p1">](../deployment/create-apply-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้แพคเกจที่สามารถปรับใช้ได้ ดู <bpt id="p1">[</bpt>ใช้แพคเกจสามารถปรับใช้ได้<ept id="p1">](../deployment/create-apply-deployable-package.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For more information about how to manually apply a deployable package, see <bpt id="p1">[</bpt>Install a deployable package<ept id="p1">](../deployment/install-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้แพคเกจที่สามารถปรับใช้ได้ด้วยตนเอง ดู <bpt id="p1">[</bpt>ติดตั้งแพคเกจที่สามารถปรับใช้ได้<ept id="p1">](../deployment/install-deployable-package.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>