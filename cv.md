# Aksana Yuzhaninava

# My contact info:
* **Adress:** Belarus, Minsk
* **Phone:** +375 33 6637478
* **E-mail:** [aksana.rusovich@gmail.com](aksana.rusovich@gmail.com)
* **GitHub:** [aksana-rus](https://github.com/aksana-rus)

# Summary
More then 3 years of experience as ABAP developer including ABAP development for HANA, Web Services‍. Solid knowledge of the ABAP Dictionary, ABAP Objects, ABAP Programming, ABAP Workbench, ALV Controls, background processing, changing the SAP standard, dialogue programming. Practical experience in development, implementation, enhancement and support of SAP products. Quite strong programming and problem analysis skills proven under high-pressure environments in external project. Effective team player with proven ability to communicate with team members and work successfully in multinational team.

# Skills
* HTML
* SAP ABAP
* OpenSQL
* SAP Gateway
* OData
  
# Code Examples
```
TABLES: SFLIGHT.
data: begin of t_data OCCURS 0.
          DATA: CARRID like SFLIGHT-CARRID, "type S_CARR_ID,
                CONNID like SFLIGHT-CONNID, "S_CONN_ID,
                FLDATE like SFLIGHT-FLDATE, "S_DATE,
 end of t_data.

  APPEND INITIAL LINE TO t_data ASSIGNING FIELD-SYMBOL(<fs>).
  <fs>-CARRID = 'AAA'.
  <fs>-CONNID = '2000'.
  <fs>-FLDATE = '10091981'.
  APPEND INITIAL LINE TO t_data ASSIGNING <fs>.
  <fs>-CARRID = 'BBB'.
  <fs>-CONNID = '2000'.
  <fs>-FLDATE = '10091981'.

  DATA lt_fieldcat TYPE slis_t_fieldcat_alv.
  DATA ls_fieldcat LIKE LINE OF lt_fieldcat.
  DATA(lr_tabdescr) = cast CL_ABAP_STRUCTDESCR( cl_abap_structdescr=>describe_by_data( t_data ) ).
  DATA(lt_dfies) = cl_salv_data_descr=>read_structdescr( lr_tabdescr ).
  LOOP AT lt_dfies INTO data(ls_dfies).
    CLEAR ls_fieldcat.
    MOVE-CORRESPONDING ls_dfies TO ls_fieldcat.
    APPEND ls_fieldcat TO lt_fieldcat.
  ENDLOOP.

  CHECK lt_fieldcat is not initial.
  LOOP AT LT_FIELDCAT ASSIGNING FIELD-SYMBOL(<fb>).
    CASE <fb>-FIELDNAME.
      WHEN 'CARRID'.
        <fb>-EDIT = 'X'.
    WHEN OTHERS.
    ENDCASE.
  ENDLOOP.
```

# Education
* Belarusian state pedagogical university named after Maksim Tank
  + Faculty of Mathematics.
* ABAP Development Lab

# Languages
* **Russian** - native spiker
* **Belarusian** - native spiker
* **Polish** - Basic
* **English** - B1
