---
layout: default
title: ID Policy
---
<h3>
  <font size=5>OBO Foundry Identifier Policy&nbsp;</font>
</h3>
<h4>
  <font color=#660000>Background</font>
</h4>
<p style="MARGIN:0.1pt 0pt">
</p>
<p style=MARGIN-LEFT:0pt;MARGIN-RIGHT:0pt>
  <font face="Arial, sans-serif"><font color=#000000><font size=2>OBO format and OWL are both valid syntaxes for OBO ontologies, and looking forward, it is the intention that these two languages be entirely interconvertible. </font></font><font face="Arial, sans-serif"><font size=2><font color=#000000>One key requirement for interconversion is that both formats use the same system for handling unique identifiers, and currently these are handled differently.</font></font></font><font color=#000000><font size=2> OBO format uses a string of the form [prefix]:nnnnnnn, while OWL uses URIs[1]. The purpose of this document is to establish a policy for OBO identifiers, a correspondence between identifiers in the two encodings, and to explain the rationale behind the choice that has been made.<br>
  </font></font></font>
</p>
<font face="Arial, sans-serif"><font color=#000000><font size=2>This policy pertains to ontologies that have been submitted to the OBO - the Open Biomedical Ontologies, also called the OBO Library</font></font></font><font face="Arial, sans-serif"><font color=#000000><font size=2> and ontologies that are part of the OBO Foundry[2]</font></font></font>
<p style=MARGIN-LEFT:0pt;MARGIN-RIGHT:0pt>
  <font size=2><br>
  </font>
</p>
<p style=MARGIN-LEFT:0pt;MARGIN-RIGHT:0pt>
  <font face="Arial, sans-serif"><font color=#000000><font size=2>The policies that are recommended here are intended to be normative for OBO Foundry ontologies and suggested for OBO Library ontologies. They do not speak to the use of OBO format for other purposes. Feedback on these policies should be sent to one of two mailing lists:&nbsp;<a href=https://lists.sourceforge.net/lists/listinfo/obo-discuss id=ob:d title=obo-discuss>obo-discuss</a>&nbsp;or&nbsp;<a href=https://lists.sourceforge.net/lists/listinfo/obo-format id=jqap title=obo-format>obo-format</a></font></font></font>
</p>
<p style=MARGIN-LEFT:0pt;MARGIN-RIGHT:0pt>
  <font size=2><br>
  </font>
</p>
<p style=MARGIN-LEFT:0pt;MARGIN-RIGHT:0pt>
  <font face="Arial, sans-serif"><font color=#000000><font size=2>This document addresses identifiers <i>only</i> for ontology terms, and not for <a href=http://www.geneontology.org/GO.format.obo-1_3.shtml#S.2.2.3 id=ynwx title=Dbxrefs>Dbxrefs</a>. It is the intention that the mapping of identifiers used in Dbxrefs will be be based on the URIs established by the <a href=http://sharedname.org/ id=jk4r title="Shared Name Initiative">Shared Name Initiative</a>.</font></font></font>
</p>
<p style=MARGIN-LEFT:0pt;MARGIN-RIGHT:0pt>
  <font size=2><br>
  </font>
</p>
<p style=COLOR:#0000ff;MARGIN-LEFT:0pt;MARGIN-RIGHT:0pt>
  <font face="Arial, sans-serif"><font color=#660000><b>Design goals&nbsp;</b></font></font>
</p>
<p style=MARGIN-LEFT:0pt;MARGIN-RIGHT:0pt>
  <font face=arial,sans-serif><font size=2><font color=#000000>There</font><font color=#000000> must be a predictable, bidirectional mapping between OBO ids, Foundry-compliant URIs, and OBO legacy URIs. </font><br>
  </font></font>
</p>
<br>
<p style=MARGIN-LEFT:0pt;MARGIN-RIGHT:0pt>
</p>
<ul>
  <li>
    <font face=arial,sans-serif><font size=2><font color=#000000>The URIs should resolve to useful information about a term.</font></font></font>
  </li>
  <li>
    <font face=arial,sans-serif><font size=2><font color=#000000>The URIs should be designed so that they can be maintained over time to keep pointing to useful information.</font></font></font>
  </li>
  <li>
    <font face=arial,sans-serif><font size=2><font color=#000000>Each OBO id is assigned to a only single term within the set of all OBO ontologies.</font></font></font>
  </li>
  <li>
    <font face=arial,sans-serif><font size=2><font color=#000000>There is a 1:1 mapping of OBO ids to Foundry-compliant URIs</font></font></font>
  </li>
</ul>
<p>
</p>
<h4>
  <font color=#660000><font face=Arial>Format of OBO format ids</font></font>
</h4>
<p style=MARGIN-LEFT:0pt;MARGIN-RIGHT:0pt>
</p>
<div id=p7ri style=TEXT-ALIGN:left>
  <div>
    <font face="Arial, sans-serif"><font size=2><font color=#000000>The syntax of OBO format ids is currently underspecified in the OBO format specification. Here is a more precise specification we will use for the purposes of this document. Some productions are adapted from the SPARQL specification. Although it is the intent that the characters used in OBO format are from Unicode, ids are further restricted to the unicode code points corresponding to ASCII characters with codes less than 128.</font></font></font>
  </div>
</div>
<div id=e8d4 style=TEXT-ALIGN:left>
  <font size=2><br>
  </font>
</div>
<div id=dcjc style=TEXT-ALIGN:left>
  <font face="'Courier New'"><font size=2><font color=#000000><b>PN_CHARS_BASE_OBO ::= [A-Z] | [a-z]&nbsp;</b></font></font></font>
</div>
<div id=cjet style=TEXT-ALIGN:left>
  <font face="'Courier New'"><font size=2><font color=#000000><b>IDSPACE ::= PN_CHARS_BASE_OBO+ ("_" PN_CHARS_BASE_OBO+ )</b><br>
  </font> </font></font>
</div>
<div id=wv:f style=TEXT-ALIGN:left>
  <font face="'Courier New'"><font size=2><font color=#000000><b>LOCALID ::= [0-9]+&nbsp;</b><br>
  </font> </font></font>
</div>
<div id=qrpt style=TEXT-ALIGN:left>
  <font face="'Courier New'"><font size=2><font color=#000000><b>OBO_IDENTIFIER ::= IDSPACE ":" LOCALID</b></font></font></font><font size=2><br>
  </font>
  <div id=ude0 style=TEXT-ALIGN:left>
    <h4>
      <font face="Arial, sans-serif"><font color=#000000><font size=2>Format of Foundry-compliant URIs</font></font></font>
    </h4>
  </div>
  <div id=j1a- style=TEXT-ALIGN:left>
    <div>
      <font face="'Courier New'"><font color=#000000><font size=2><b>FOUNDRY_OBO_URI ::= "http://purl.obolibrary.org/obo/" IDSPACE "_" LOCALID</b></font></font></font>
    </div>
  </div>
  <div id=s717 style=TEXT-ALIGN:left>
    <h4>
      <font face="Arial, sans-serif"><font color=#000000><font size=2>Format of OBO legacy URIs</font></font></font>
    </h4>
    <font face="Arial, sans-serif"><font color=#000000><font size=2>Those are found in documents that</font><font size=2>&nbsp;were natively authored using the OBO format and which were converted using the NCBOoboInOwl script before this policy was put in place. </font></font></font><br>
    <br>
  </div>
  <div id=d2yu style=TEXT-ALIGN:left>
    <div>
      <font face="'Courier New'"><font color=#000000><font size=2><b>LEGACY_OBO_URI ::= "http://purl.org/obo/owl/" IDSPACE "#" IDSPACE "_" LOCALID</b></font></font></font>
    </div>
  </div>
  <h4>
    <font face="Arial, sans-serif"><font size=2><font color=#000000>Mapping of OWL ids to OBO format ids</font></font></font>
  </h4>
  <p>
    <font face="Arial, sans-serif"><font size=2><font color=#000000>The mappings between OBO format, Foundry-compliant URIs, and OBO legacy URIs are shown in Figure 1.&nbsp;</font></font></font>
  </p>
  <div id=wwjr style=TEXT-ALIGN:left>
    <img src="id-relationship.png" style=HEIGHT:257px;WIDTH:515px>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font face="Arial, sans-serif"><font size=2><font style=BACKGROUND-COLOR:#ffffff><font color=#000000>Figure 1. Mappings between OBO format ids and URIs.</font><br>
    </font></font></font>
  </div>
  <font size=2><br>
  </font>
</div>
<div id=etrd style=TEXT-ALIGN:left>
  <div>
    <font face="Arial, sans-serif"><font size=2><font color=#000000>The mappings between OBO format, Foundry-compliant URIs, and OBO legacy URIs &nbsp;is defined in terms of a regular expression substitution using Perl syntax.&nbsp;</font></font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font face="Arial, sans-serif"><font size=2>1. From OBO format to Foundry-compliant URI:&nbsp;</font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font face="'Courier New'"><font size=2><b>&nbsp;&nbsp; &nbsp;s/((</b><font size=2><font face="arial, sans-serif">[A-Za-z_]*</font></font><b>):(\d+))/</b></font></font><font face="'Courier New'"><font size=2><b>http:\/\/purl.obolibrary.org\/obo\/$1_$2/</b><br>
    </font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font face="Arial, sans-serif"><font size=2>2. From OBO format to OBO legacy URI:&nbsp;</font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font face="'Courier New'"><font size=2><b>&nbsp;&nbsp; &nbsp;s/((</b><font size=2><font face="arial, sans-serif">[A-Za-z_]*</font></font><b>):(\d+))/</b></font></font><font face="'Courier New'"><font size=2><b>http:\/\/purl.org\/obo\/owl\/$1#$1_$2/</b><br>
    </font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font face="Arial, sans-serif"><font size=2>3. From Foundry-compliant URI to OBO format:&nbsp;</font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font face="'Courier New'"><font size=2><b>&nbsp;&nbsp; &nbsp;s/</b></font></font><font face="'Courier New'"><font size=2><b>http:\/\/purl.obolibrary.org\/obo\/(</b><font size=2><font face="arial, sans-serif">[A-Za-z_]*</font></font><b>)_(\d+)/$1:$2/</b></font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font face=arial,sans-serif><font size=2>4. From&nbsp;</font><font size=2>OBO legacy URI</font><font size=2>&nbsp;to Foundry-compliant URI:&nbsp;</font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font face="'Courier New'"><font size=2><b>&nbsp;&nbsp; &nbsp;s/</b></font></font><font face="'Courier New'"><font size=2><b>http:\/\/purl.org\/obo\/owl\/([^#]+)#\1_(</b><font size=2><font face="arial, sans-serif">[A-Za-z_]*</font></font><b>)/http:\/\/purl.obolibrary.org\/obo\/$1_$2/</b></font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font face=arial,sans-serif><font size=2>5. From&nbsp;</font><font size=2>Foundry-compliant&nbsp;</font><font size=2>URI to OBO legacy URI:&nbsp;</font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font face="'Courier New'"><font size=2><b>&nbsp;&nbsp; &nbsp;s/</b></font></font><font face="'Courier New'"><font size=2><b>http:\/\/purl.obolibrary.org\/obo\/(</b><font size=2><font face="arial, sans-serif">[A-Za-z_]*</font></font><b>)_(\d+)/http:\/\/purl.org\/obo\/owl\/$1#$1_$2/</b></font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <div>
      <font face=arial,sans-serif><font size=2>6.&nbsp;<font size=2>From&nbsp;</font><font size=2>OBO legacy URI</font>&nbsp;to OBO format:&nbsp;</font></font>
    </div>
    <font size=2><br>
    </font>
    <div>
      <font face="'Courier New'"><b>&nbsp;&nbsp; &nbsp;</b><font size=2><b>s</b></font></font><font face="'Courier New'"><font size=2><font face="'Courier New'"><font size=2><b>/</b></font></font><font face="'Courier New'"><font size=2><b>http:\/\/purl.org\/obo\/owl\/([^#]+)#\1_(</b><font size=2><font face="arial, sans-serif">[A-Za-z_]*</font></font><b>)</b></font></font><b>/$1:$2/</b></font></font>
    </div>
    <font size=2><br>
    <font face=arial,sans-serif><font color=#000000>Using these rules the OBO id&nbsp;</font></font><font face=arial,sans-serif><font color=#000000><b>GO:</b></font></font><font face=arial,sans-serif><font color=#000000><b>0050918</b></font></font><font face=arial,sans-serif><font color=#000000> is mapped to<br>
    &nbsp;&nbsp; &nbsp;a) the Foundry-compliant URI </font></font><font face=arial,sans-serif><font color=#000000><b>http://purl.obolibrary.org/obo/GO_0050918</b></font></font><font face=arial,sans-serif><font color=#000000> and<br>
    &nbsp;&nbsp; &nbsp;b) the OBO legacy URI </font></font><font face=arial,sans-serif><font color=#000000><b>http://purl.org/obo/owl/GO#GO_0050918</b></font></font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font color=#660000><font face="Arial, sans-serif"><b>idspace directive in OBO Format file</b></font></font>
  </div>
  <br>
  <div>
    <font face="Arial, sans-serif"><font color=#000000>The idspace directive [6,7,8] in OBO format associates a prefix with a URI. idspace directives can be omitted in OBO format files, for those <b><font face="courier new">IDSPACE</font></b>s that are allocated to OBO ontologies. If present they <b>MUST</b> agree with the mappings above.<br>
    </font></font><br>
  </div>
  <div>
    <font color=#660000><font face="Arial, sans-serif"><b>ID expressions and xref header directives in OBO Format files</b></font></font>
  </div>
</div>
<div style=TEXT-ALIGN:left>
  <br>
  <div>
    <font face="Arial, sans-serif"><font color=#000000><i><b>Note: This section references OBO specification version 1.3, which is deprecated. Readers should consider this section as background material.</b></i></font>
</div>
<div id=d6ka style=TEXT-ALIGN:left>
  <br>
  <div>
    <font face="Arial, sans-serif"><font color=#000000>OBO 1.3 [7,8] introduces identifier expressions that can be taken as a kind of macro that expands into a logical definition. Although the surface syntax of id expressions conforms to the OBO format for identifiers they are not considered identifiers but rather shorthand for un-named class expressions which should be expanded (see [8] sec 4.1) <font color=#0000ff>MC: [8] 4.1 is "</font></font></font><font color=#0000ff>4.1 Relation to OBO-Format 1.2 "</font><font color=#0000ff>&nbsp; Should it be 4.11? </font><font color=#b45f06>AR: TOC of sync: Chris FIXME</font>&nbsp;<font face="Arial, sans-serif"><font color=#000000>before applying the id mapping policy. Therefore the mappings above do not apply to id expressions. Note: Although the draft OBO 1.3 specification allows id expressions to function as normal ids, including being associated with annotations such as label and definition, this will likely be revised to disallow such use.<br>
    <br>
    </font></font>
    <p>
      Example of ID Definitional Expressions: <b>GO:0005737^part_of(CL:0000023)</b> can be used wherever one wants to say "cytoplasm of oocyte". This is treated as if it has the following definition:
    </p>
    <div class=fmt>
      <p>
        <font face="Courier New"> [Term]<br>
        id: GO:0005737^part_of(CL:0000023)<br>
        intersection_of: GO:0005737 ! cytoplasm<br>
        intersection_of: part_of CL:0000023 ! oocyte </font>
      </p>
    </div>
    <br>
  </div>
  <br>
  <div>
    <font face="Arial, sans-serif"><font color=#000000>OBO 1.3 defines a further transformation that can affect the parsing of strings that on the surface might be transformed as identifiers, according to the mapping rules described above. Transformations specified by these directives, described in [8] sec 4.11, should be applied <b>before </b>interpreting any ids in an OBO format file. After transformation, ids should comply with the ID policy.</font></font><br>
  </div>
  <br>
  <div>
    <font face="Arial, sans-serif"><font color=#000000>The process of "expanding" an OBO format file by applying the header directives for xrefs and to interpret identifier expressions, should be considered a source transform that given an OBO Format file with such elements, creates a new OBO Format file without any xref header directives or identifier expressions. Any mappings of identifiers are applicable to the resultant OBO Format file that is the result of such an expansion.</font></font>
  </div>
  <br>
  <div>
    <font face="Arial, sans-serif"><font color=#660000><b>Policy for OBO Foundry ontologies</b></font></font>
  </div>
  <br>
</div>
<p>
  <font face="Arial, sans-serif"><font size=2>OBO Foundry ontologies MUST use OBO format identifiers that match the production&nbsp;<b>OBO_IDENTIFIER&nbsp;</b><font face=arial,sans-serif>if they are formatted in OBO format, and the production<b>&nbsp;FOUNDRY_OBO_URI</b><font face=arial,sans-serif>&nbsp;if they are formatted as OWL. Where an ontology is distributed in both formats, identifiers are mapped according to the substitutions defined in the section "Mapping of OWL ids to OBO format ids".</font></font></font></font>
</p>
<p>
  <font size=2><br>
  </font>
</p>
<p>
  <font color=#660000><b>Response to Web requests for OBO URIs</b></font>
</p>
<p>
</p>
<p>
  <font face=Arial><font size=2>It is expected that the Foundry-compliant URIs behave, on the web, usefully.&nbsp; It will be the role of the </font></font><font face=Arial><font size=2>OBO Foundry to supply generic software for responding to requests at URIs that identify OBO terms.<br>
  </font></font>
</p>
<p>
  <font size=2><br>
  </font>
</p>
<p>
  <font face=Arial><font size=2>We borrow the criteria from the Shared Name Initiative (</font></font><font face=arial>http://sharedname.org/)</font><font face=Arial><font size=2>&nbsp;as a base line. The OBO Foundry may issue further recommendations if experience shows them to be considered generally useful.</font></font>
</p>
<p>
  <font size=2><br>
  </font>
</p>
<p>
</p>
<ol style=MARGIN-LEFT:20px>
  <li>
    <p>
      <font face=Arial>It must be clearly stated what the intended referent of each URI is supposed to be, i.e. that the URI denotes some particular record from some particular database.</font>
    </p>
  </li>
  <li>
    <p>
      <font face=Arial>Information about the URI and its referent, including such a statement, must be made available, and in order to leverage existing protocol stacks, it must be obtainable via HTTP. (We will call such information "URI documentation".)</font>
    </p>
  </li>
  <li>
    <p>
      <font face=Arial>URI documentation must be provided in RDF.</font>
    </p>
  </li>
  <li>
    <p>
      <font face=Arial>Provision of URI documentation must be an ongoing concern. The ability to provide it may have to outlive the original ontology developer's group or creator.</font>
    </p>
  </li>
  <li>
    <p>
      <font face=Arial>The provider of the URI documentation must be responsive to community needs, such as the need to have mistakes fixed in a timely manner.<br>
      </font>
    </p>
  </li>
  <li>
    <p>
      <font face=Arial>URI documentation must be open so that it can be replicated and reused.</font>
    </p>
  </li>
</ol>
<p>
</p>
<p>
  <font size=2><br>
  </font>
</p>
<p>
  <font face=Arial><font size=2>Individual ontology projects may, at their discretion, choose to manage these responses, with the understanding that if service lapses the Foundry may substitute the generic software for handling them in order to maintain service.</font></font>
</p>
<h4>
  <font color=#660000>Policy for OBO Library ontologies</font>
</h4>
<p>
</p>
<div>
  <p>
    <font face="Arial, sans-serif"><font size=2>OBO Library ontologies are not constrained by this policy, however, we recommend that they follow it nonetheless, for three reasons. First, it provides a uniform experience and sets expectations for ontology clients. Second, by doing so library ontologies will be able to take advantage of shared infrastructure. Third, ontologies that eventually join the foundry would have to disrupt their ids if they had to change to follow this policy.</font></font>
  </p>
  <p>
    <br>
  </p>
  <p>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font color=#660000><b>Allocating IDSPACEs</b></font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <b><br>
    </b>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font color=#000000>IDSPACEs within the OBO library are unique for a given project and are chosen not to conflict with prefix for xrefs. Although IDSPACEs are case-sensitive, there will never be more than one IDSPACEs that are the same when compared in a case-insensitive manner. Therefore,&nbsp;<font size=2><font face="helvetica, sans-serif">although "GO" and "go", "Go" and &nbsp;"gO" are different IDSPACEs, the IDSPACE "go", "Go" and &nbsp;"gO" will not be used as "GO" has already been allocated.&nbsp;</font></font></font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <br>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font color=#000000><font size=2><font face="arial, sans-serif">A registry of allocated IDSPACEs will be maintained. Requests for an IDSPACE should be made by sending mail to obo-discuss@lists.sourceforge.net, cc obo-admin@fruitfly.org. A request should include information about the ontology, such as scope and maintainer and a confirmation that the ontology is open access.</font></font></font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <br>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font color=#660000><b>Resources at Known locations</b></font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <b><br>
    </b>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>Registry of IDSPACEs: http://purl.obolibrary.org/obo/idspaces.txt</font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2><br>
    </font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>A tab delimited text file with five columns,&nbsp;</font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <br>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>1) the idspace,&nbsp;</font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>2) a string indicating the status of the idspace. The possible values for status are&nbsp;</font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>&nbsp;&nbsp; &nbsp;"OBOFOUNDRY" - The IDSPACE is of an OBO Foundry ontology</font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>&nbsp;&nbsp; &nbsp;"OBOLIBRARY" - The IDSPACE is of an OBO ontology, not currently a Foundry ontology</font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>&nbsp;&nbsp; &nbsp;"RESERVED" - The IDSPACE is used for dbxrefs or is otherwise unsuitable as an idspace for an ontology&nbsp;</font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>3) The name of the point of contact</font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>4) The email address for the point of contact</font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>5) A short description of the scope</font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2><br>
    </font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2><b>Current ontology document:</b></font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2><br>
    </font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>The most current version of an ontology will be at the following URL, where "IDSPACE" is replaced with the IDSPACE of the given ontology in lower case.</font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2><br>
    </font>
  </p>
  <p style=MARGIN-LEFT:0px;MARGIN-RIGHT:0px>
    <font size=2>&nbsp;&nbsp;Current OWL: http://purl.obolibrary.org/obo/IDSPACE.owl</font>
  </p>
  <div>
    <b>&nbsp;&nbsp;</b><font color=#000000><font size=2>Current OBO: http://purl.obolibrary.org/obo/IDSPACE.obo</font></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <font size=2>For example, the Ontology for Biomedical Investigations has the IDSPACE "OBI", so the current version of the OWL document would be at <a href=http://purl.obolibrary.org/obo/obi.owl id=uvm: title=http://purl.obolibrary.org/obo/obi.owl>http://purl.obolibrary.org/obo/obi.owl</a></font>
  </div>
  <br>
  <div>
    <font size=2><b>Ontology subsets and variants:</b></font>
  </div>
  <b><br>
  </b>
  <div>
    <font size=2>Aside from the standard version, an ontology may provide differently packaged elements of the ontology, or ontology versions with additional contents. For example</font>
  </div>
  <div>
    &nbsp;&nbsp; &nbsp;
  </div>
  <div>
    <font size=2>&nbsp;&nbsp; &nbsp;- Subsets of the ontology tailored to particular purposes or user communities, sometimes called subsets, slims, views, or modules.</font>
  </div>
  <div>
    <font size=2>&nbsp;&nbsp; &nbsp;- A version with or without inferred relations as part of it<br>
    </font>
  </div>
  <div>
    <font size=2>&nbsp;&nbsp; &nbsp;- A version that includes more or less metadata, such as change tracking<br>
    </font>
  </div>
  <div>
    <font size=2>&nbsp;&nbsp; &nbsp;- Pre-release work or experimental extensions<br>
    </font>
  </div>
  <br>
  The current version of such additional artifacts should be accessible at URIs with the prefix&nbsp;
</div>
<br>
<div>
  <font size=2>&nbsp;&nbsp; &nbsp;http://purl.obolibrary.org/obo/&lt;idspace&gt;/&lt;name&gt;.owl</font><br>
  <font size=2>&nbsp;&nbsp; &nbsp;http://purl.obolibrary.org/obo/&lt;idspace&gt;/&lt;name&gt;.obo</font>
</div>
<br>
<div>
  <font size=2>Where<font size=2>&nbsp;&lt;idspace&gt; is replaced by the IDSPACE in lower case, and &lt;name&gt; is the name for the artifact.</font></font>
</div>
<br>
<p style=FONT-FAMILY:helvetica;FONT-STYLE:normal;MARGIN:0px>
  <font size=2><font size=2>For example, IAO distributes its ontology metadata set as a distinct document, with &lt;name&gt; "ontology-metadata"</font></font>
</p>
<div>
  <font size=2><br>
  </font>
  <div>
    <font size=2><b>Versions of ontologies:</b>&nbsp;</font>
  </div>
  <b><br>
  </b>
  <div>
    Versions are named by a date in the following format: YYYY-MM-DD. For a given version of an ontology, the ontology should be accessible at the following URL, where &lt;idspace&gt; is replaced by the IDSPACE in lower case
  </div>
  <br>
  <div>
    &nbsp;&nbsp;<font size=2>OWL: http://purl.obolibrary.org/obo/&lt;idspace&gt;/YYYY-MM-DD/&lt;idspace&gt;.owl</font>
  </div>
  <div>
    &nbsp;&nbsp;<font size=2>OBO: http://purl.obolibrary.org/obo/&lt;idspace&gt;/YYYY-MM-DD/&lt;idspace&gt;.obo</font>
  </div>
  <br>
  <font size=2>For example, for the version of OBI released 2009-11-06, the OWL document is accessible at&nbsp;<a href=http://purl.obolibrary.org/obo/obi/2009-11-06/obi.owl id=ywlp title=http://purl.obolibrary.org/obo/obi/2009-11-06/obi.owl>http://purl.obolibrary.org/obo/obi/2009-11-06/obi.owl</a></font>
</div>
<div>
  <a href=http://purl.obolibrary.org/obo/obi/2009-11-06/obi.owl id=kt.j title=http://purl.obolibrary.org/obo/obi/2009-11-06/obi.owl></a><br>
  <div>
    <font size=2>Ontology variants are versioned in the same manner. URIs for a given version would have the version date between &lt;idspace&gt; and &lt;name&gt;. For example.</font>
  </div>
  <br>
  &nbsp;&nbsp;<font size=2>http://purl.obolibrary.org/obo/iao/ontology-metadata.owl for the version of date 2009-11-02 would have the URI</font>
</div>
<div>
  <font size=2>&nbsp;&nbsp;http://purl.obolibrary.org/obo/iao/2009-11-02/ontology-metadata.owl</font>
</div>
<div>
  &nbsp;&nbsp;<font size=2><br>
  </font><br>
  <div>
    <b><font size=2>Home page:</font></b>
  </div>
  <b><font size=2><br>
  </font></b>
  <div>
    <font size=2>If the ontology has a home page on the Web, it is accessible at http://purl.obolibrary.org/obo/IDSPACE. For example the OBI home page is accessible at: <a href=http://purl.obolibrary.org/obo/obi id=g_6. title=http://purl.obolibrary.org/obo/obi>http://purl.obolibrary.org/obo/obi</a></font>
  </div>
  <b><font size=2><br>
  </font></b>
  <div>
    <b><font size=2>Tracker:</font></b>
  </div>
  <b><font size=2><br>
  </font></b>
  <div>
    <font size=2>If the ontology has a tracker for submitting an monitoring term and other requests, it is accessible at http://purl.obolibrary.org/obo/IDSPACE/tracker. For example the OBI tracker is accessible at: <a href=http://purl.obolibrary.org/obo/obi/tracker id=v3lx title=http://purl.obolibrary.org/obo/obi/tracker>http://purl.obolibrary.org/obo/obi/tracker</a></font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <b><font size=2>Browse:</font></b>
  </div>
  <b><font size=2><br>
  </font></b>
  <div>
    <font size=2>If the ontology developers provide or suggest a way of browsing the ontology, it is accessible at http://purl.obolibrary.org/obo/IDSPACE/browse. For example the OBI project suggests people browse OBI using the NCBO Bioportal, and so <a href=http://purl.obolibrary.org/obo/obi/browse id=aqze title=http://purl.obolibrary.org/obo/obi/browse>http://purl.obolibrary.org/obo/obi/browse</a> redirects to the Bioportal view on OBI.</font>
  </div>
  <font size=2><br>
  </font>
  <div>
    <b><font size=2>Wiki:</font></b>
  </div>
  <b><font size=2><br>
  </font></b>
  <div>
    <font size=2>If the ontology developers provide a development wiki, it is accessible at http://purl.obolibrary.org/obo/IDSPACE/wiki. For example the OBI project wiki is accessible at <a href=http://purl.obolibrary.org/obo/obi/wiki id=hexs title=http://purl.obolibrary.org/obo/obi/wiki>http://purl.obolibrary.org/obo/obi/wiki</a>.<br>
    <br>
    </font>
  </div>
  <p>
  </p>
  <p>
    <font color=#660000><b>History and Rationale</b></font>
  </p>
  <p>
    <b><br>
    </b>
  </p>
  <font face=arial id=pz2w size=2>This policy was initially discussed, drafted and implemented as part of the development of the Ontology for Biomedical Investigations (OBI, </font><font size=2><a class="external free" href=http://purl.obolibrary.org/obo/obi rel=nofollow style=FONT-FAMILY:Arial title=http://purl.obolibrary.org/obo/obi>http://purl.obolibrary.org/obo/obi</a></font><font face=arial id=ae37 size=2>) project.<br>
  <br>
  Their goal was to provide stable and homogeneous identifiers for OBI entities, and to be able </font><font size=2><font face=arial>to respond with providing a bounded amount of useful information for each URI denoting a term in OBI.&nbsp;<font size=2>The project chose[3] to use purl [4] based URIs, because of the ability to redirect to a different URL should we want to change hosts, etc. </font><font size=2>To protect ourselves against a future time when purl.org might not be as reliable, or in case we wish to substitute a different technology for resolving term requests, we use our own domain name, and have the DNS [5] point to purl.org.</font></font></font>
</div>
<font size=2><br>
</font>
<p style="FONT-FAMILY:Arial;MARGIN:0.1pt 0pt">
  The hostname chosen for this by vote of the OBO Foundry editors is <font size=2>purl.obolibrary.org. This dedicated hostname allows redirection at the DNS level, so that we don't require extra time for the resolution or dedicated servers to actually handle lookups.<br>
  &nbsp;</font>
</p>
<p style="FONT-FAMILY:Arial;MARGIN:0.1pt 0pt">
  <font size=2>While the initial preference was towards maintaining IDs as currently used by the community (e.g. GO:nnnnnnn), RDF/XML and N3 (the other RDF syntax) require the character after the colon to be alphabetic. (see <a href=http://www.w3.org/TR/REC-xml-names/#NT-QName id=qa_n title="Namespaces in XML">QName production in the W3C specification Namespaces in XML</a>&nbsp;and productions [7][8][11][4][6] - the last&nbsp;<font size=2>[6] NCNameStartChar ::= Letter | '_' &nbsp;is responsible for the prohibition against leading digit)<br>
  </font><font size=2><br>
  </font></font>
</p>
<p>
  <font face=arial><font size=2>All entities that we define - classes, relations, and instances - are assigned IDs. URIs are opaque, </font></font><font face=arial><font size=2>and we use labels for the human readable version. Editing tools can then be configured to display the labels instead of the identifiers.<br>
  </font></font>
</p>
<p style="MARGIN:0.1pt 0pt">
  <br>
</p>
<p style="MARGIN:0.1pt 0pt">
  <font face=arial><font size=2>Note that the OBO legacy URIs will be supported for dereferencing ontologies for some transition period, however applications that depend on referencing OBO ontology terms using the legacy URI will need to migrate to using Foundry-compliant URIs for ontologies that choose to use them.</font></font>
</p>
<p style="MARGIN:0.1pt 0pt">
  <font size=2><br>
  </font>
</p>
<p style="MARGIN:0.1pt 0pt">
</p>
<p style="MARGIN:0.1pt 0pt">
  <font face=arial><font size=2>The OBO legacy URIs are of the form </font></font><font face=arial><font size=2><a href=http://purl.org/obo/owl/OBI#OBI_0100051 title=http://purl.org/obo/owl/OBI#OBI_0100051>http://purl.org/obo/owl/OBI#OBI_0100051</a><font color=#0000ff>.</font></font></font>
</p>
<p style="MARGIN:0.1pt 0pt">
  <font size=2><br>
  </font>
</p>
<p style="MARGIN:0.1pt 0pt">
  <font size=2>Undesirable aspects of the OBO legacy URIs are:&nbsp;</font>
</p>
<p style="MARGIN:0.1pt 0pt">
  <font size=2><br>
  </font>
</p>
<ul type=disc>
  <li>
    <font face=arial><font size=2>"owl" isn't a necessary part of the name.</font></font>
  </li>
  <li>
    <font face=arial><font size=2>"OBI" appears redundantly in the URI</font></font>
  </li>
  <li>
    <font face=arial><font size=2>The # doesn't scale if we want to provide web pages per term. What it means in the URI is that one should fetch the whole ontology, and then look up the part after the "#" - the "fragment identifier". For ontologies such as FMA, this is a real problem</font></font>
  </li>
</ul>
<p>
  <font face=arial><font size=2><br>
  The adopted format, <a href=http://purl.obolibrary.org/obo/OBI_0100051 id=u_sf title=http://purl.obolibrary.org/obo/OBI_0100051>http://purl.obolibrary.org/obo/OBI_0100051</a>, is as short as sensible while avoiding the above issues.</font></font>
</p>
<p id=irl9 style=FONT-FAMILY:Arial;MARGIN-LEFT:0.64cm>
  <font size=2><br>
  </font>
</p>
<p id=wwl. style=FONT-FAMILY:Arial>
  <font id=w_y4 size=2><b><font color=#660000>References<br>
  </font></b></font>
</p>
<p id=mcvg style=FONT-FAMILY:Arial>
  <font size=2><br id=n462>
  </font>
</p>
<p id=r61l style=FONT-FAMILY:Arial>
  <font size=2> [1] http://en.wikipedia.org/wiki/Uniform_Resource_Identifier, a <b>Uniform Resource Identifier</b> (<b>URI</b>) consists of a <a class=mw-redirect href=http://en.wikipedia.org/wiki/Character_string_%28computer_science%29 title="Character string (computer science)">string</a> of <a href=http://en.wikipedia.org/wiki/Character_%28computing%29 title="Character (computing)">characters</a> used to <a href=http://en.wikipedia.org/wiki/Identifier title=Identifier>identify</a> or name a <a href=http://en.wikipedia.org/wiki/Resource_%28Web%29 title="Resource (Web)">resource</a> on the <a href=http://en.wikipedia.org/wiki/Internet title=Internet>Internet</a>. Such identification enables interaction with representations of the resource over a network (typically the <a href=http://en.wikipedia.org/wiki/World_Wide_Web title="World Wide Web">World Wide Web</a>) using specific <a href=http://en.wikipedia.org/wiki/Protocol_%28computing%29 title="Protocol (computing)">protocols</a>.</font>
</p>
<p id=h6sr style=FONT-FAMILY:Arial>
  <font size=2><br>
  </font>
</p>
<p id=x3it style=FONT-FAMILY:Arial>
  <font size=2>[2] <a href=http://www.ncbi.nlm.nih.gov/pubmed/17989687 id=a536 title="The OBO Foundry: coordinated evolution of ontologies to support biomedical data integration">The OBO Foundry: coordinated evolution of ontologies to support biomedical data integration</a>.</font>
</p>
<p id=pvd. style=FONT-FAMILY:Arial>
  <br>
</p>
<p id=k0:6 style=FONT-FAMILY:Arial>
  <font size=2>[3]&nbsp;</font><a href=http://groups.google.com/group/obi-developer/browse_thread/thread/178768c384f4e9c6?hl=en id=gbom style=COLOR:#551a8b title="changing OBI's URIs to be purl based"><font size=2>Changing OBI's URIs to be purl based</font></a><font size=2>&nbsp;- discussion on obi-developers list</font>
</p>
<p id=jsp6 style=FONT-FAMILY:Arial>
  <br>
  <font color=#000000 id=ljz9 size=2>[4] <a href=http://purl.org/ id=z_ip>http://purl.org/</a>, A PURL is a <b>P</b>ersistent <b>U</b>niform <b>R</b>esource <b>L</b>ocator. Functionally, a PURL is a URL. However, instead of pointing directly to the location of an Internet resource, a PURL points to an intermediate resolution service. The PURL resolution service associates the PURL with the actual URL and returns that URL to the client. The client can then complete the URL transaction in the normal fashion. In Web parlance, this is a standard HTTP <i>redirect</i>.</font>
</p>
<p id=iav9 style=FONT-FAMILY:Arial>
  <font size=2><br id=owf:>
  </font>
</p>
<p id=p7sr style=FONT-FAMILY:Arial>
  <font id=g9mr size=2>[5] <a href=http://en.wikipedia.org/wiki/Domain_name_system id=vq6t>http://en.wikipedia.org/wiki/Domain_name_system</a>, </font><font id=b.f2 size=2>the </font><font id=l231 size=2><b>Domain Name System</b></font><font id=ctgg size=2> (DNS) associates various sorts of information with so-called <a href=http://en.wikipedia.org/wiki/Domain_name id=i83s>domain names</a>; most importantly, it serves as the "<a href=http://en.wikipedia.org/wiki/Telephone_directory id=m36t>phone book</a>" for the Internet by translating human-readable computer <a href=http://en.wikipedia.org/wiki/Hostname id=fivc>hostnames</a>, e.g. <a href=http://en.wikipedia.org/wiki/Example.com id=k3wc><i>www.example.com</i></a></font><font id=k2cm size=2>, into the <a href=http://en.wikipedia.org/wiki/IP_address id=iu23>IP addresses</a>, e.g. </font><font id=ly90 size=2><i>208.77.188.166</i></font><font id=x:l4 size=2>, that networking equipment needs to deliver information.</font>
</p>
<p id=u5ka style=FONT-FAMILY:Arial>
  <font size=2><br>
  </font>
</p>
<p id=os8a style=FONT-FAMILY:Arial>
  <font size=2>[6] The OBO Flat File Format Specification, version 1.2 <a href=http://www.geneontology.org/GO.format.obo-1_2.shtml id=h2f9 title=http://www.geneontology.org/GO.format.obo-1_2.shtml>http://www.geneontology.org/GO.format.obo-1_2.shtml</a></font>
</p>
<p id=ajxd style=FONT-FAMILY:Arial>
  <font size=2><br>
  </font>
</p>
<p id=m6jd style=FONT-FAMILY:Arial>
  <font size=2>[7] The OBO Flat File Format Specification, version 1.3 draft: <a href=http://www.geneontology.org/GO.format.obo-1_3.shtml id=oyj- title=http://www.geneontology.org/GO.format.obo-1_3.shtml>http://www.geneontology.org/GO.format.obo-1_3.shtml</a></font>
</p>
<p id=whhz style=FONT-FAMILY:Arial>
  <font size=2><br>
  </font>
</p>
<p id=nt5s style=FONT-FAMILY:Arial>
  <font size=2>[</font><font color=#660000><font color=#000000><font size=2>8] OBO-Format and Obolog Specification (1.3) </font></font><font color=#000000><font size=2>DRAFT <a href=http://oboedit.org/obolog/spec/obolog-spec.pdf id=zvvy title=http://oboedit.org/obolog/spec/obolog-spec.pdf>http://oboedit.org/obolog/spec/obolog-spec.pdf</a><br>
  </font></font><font size=2><br>
  </font><font size=2><br>
  </font><b><font size=2>Acknowledgments</font></b></font>
</p>
<p id=ijmj style=FONT-FAMILY:Arial>
  <font id=xmwu size=2>This policy has been initially discussed, drafted and implemented as part of the development of the OBI project.</font>
</p>
<font color=#000000 face=arial id=cxzy size=2>Authors: Alan Ruttenberg, </font><font color=#000000 face=arial id=u.3. size=2>Melanie Courtot </font><font id=ataz size=2><font face=arial>and Chris Mungall.</font></font>
<p id=pla7 style=FONT-FAMILY:Verdana>
  <font id=t1iv size=2><font face=arial>Thanks to Jonathan Rees, </font></font><font color=#000000 face=arial id=ugl2 size=2>Bill Bug, Colin Batchelor, David Osumi-Sutherland, Duncan Hull, Peter Robinson, Michel Dumontier, the OBO coordinators and the OBI Consortium</font><font id=nwjy size=2><font face=arial> for their help.</font></font>
</p>
</div>

