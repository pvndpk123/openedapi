OpenEd API
==========

OpenEd is the world's largest educational resource catalog.  It is the only site completely focused on aligning educational resources to standards.   

The OpenEd API lets you use the capabilities of the OpenEd engine for finding resources and providing information about educational standards (Common Core and otherwise) inside your own apps and websites.

All API access is over HTTPS, and accessed from the api.opened.io domain. All data is sent and received as JSON.  API calls which make changes require OAuth 2 authentication.

Find Resources
--------------

Find resources based on:
* ids - comma separated list of resource IDs
* descriptive - searches title and description fields with fuzzy match
* grade - restricts to specified grades (expressed as K,1, ..12)
* standard - looks for resources aligned with specified standard (can be combined)
* user - unique ID of user, for logging purposes
* number of resources to return, defaults to 20

For example:

` https://api.opened.io/resources.json?descriptive=Quadratic%20Equations `

will return a JSON object like the following

```json
[{"area_id":null,"description":null,"embeddable":true,"id":337744,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/337744/thumb/wqRM039Y3ZQ.?1373634781","thumb_status":null,"title":"From Equation to Words","youtube_id":"wqRM039Y3ZQ","safe_url":"https://www.youtube.com/watch?v=wqRM039Y3ZQ","contribution_name":"YouTubeMrAlmeida","grade_idents":[],"standard_idents":[],"grades_range":"","resource_type_title":"Video","area_title":null,"subject_titles":[],"grades":[],"standards":[]},{"area_id":null,"description":null,"embeddable":true,"id":337750,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/337750/thumb/ocaJ6yqy41o.?1373645310","thumb_status":null,"title":"Factor Quadratics","youtube_id":"ocaJ6yqy41o","safe_url":"https://www.youtube.com/watch?v=ocaJ6yqy41o","contribution_name":"YouTubeMrAlmeida","grade_idents":[],"standard_idents":[],"grades_range":"","resource_type_title":"Video","area_title":null,"subject_titles":[],"grades":[],"standards":[]},{"area_id":1,"description":null,"embeddable":false,"id":223672,"imported_area_id":40,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/223672/thumb/favicon.png?1370856993","thumb_status":null,"title":"Incorrect equation","youtube_id":null,"safe_url":"http://braingenie.ck12.org/skills/102791","contribution_name":"BrainGenie","grade_idents":["4","5"],"standard_idents":["4.MD.1","5.MD.1"],"grades_range":"4-5","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Measurement & Data"],"grades":[{"grade":"4"},{"grade":"5"}],"standards":[{"identifier":"4.MD.1"},{"identifier":"5.MD.1"}]},{"area_id":null,"description":null,"embeddable":false,"id":226150,"imported_area_id":41,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/226150/thumb/favicon.png?1370844871","thumb_status":null,"title":"Simultaneous Equations","youtube_id":null,"safe_url":"http://braingenie.ck12.org/skills/103459","contribution_name":"BrainGenie","grade_idents":[],"standard_idents":[],"grades_range":"","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Algebra"],"grades":[],"standards":[]},{"area_id":1,"description":"","embeddable":true,"id":116047,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/116047/thumb/default.jpg?1359200462","thumb_status":null,"title":"Equation For a Circle","youtube_id":"HjN9TTRrQiA","safe_url":"https://www.youtube.com/watch?v=HjN9TTRrQiA","contribution_name":"YouTube","grade_idents":["9","10","11","12"],"standard_idents":["G.C.1"],"grades_range":"9-12","resource_type_title":"Video","area_title":"Mathematics","subject_titles":["Geometry"],"grades":[{"grade":"9"},{"grade":"10"},{"grade":"11"},{"grade":"12"}],"standards":[{"identifier":"G.C.1"}]},{"area_id":1,"description":null,"embeddable":false,"id":183426,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/183426/thumb/KhanAcademy.jpeg?1362719117","thumb_status":null,"title":"Systems of equations","youtube_id":null,"safe_url":"http://www.khanacademy.org/exercise/systems_of_equations","contribution_name":"KhanAcademyCommonCore","grade_idents":["8","9","10","11","12"],"standard_idents":["8.EE.8","8.EE.8.a","8.EE.8.b","8.EE.8.c","A.CED.3","A.REI.6"],"grades_range":"8-12","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Algebra"],"grades":[{"grade":"8"},{"grade":"9"},{"grade":"10"},{"grade":"11"},{"grade":"12"}],"standards":[{"identifier":"8.EE.8"},{"identifier":"8.EE.8.a"},{"identifier":"8.EE.8.b"},{"identifier":"8.EE.8.c"},{"identifier":"A.CED.3"},{"identifier":"A.REI.5"},{"identifier":"A.REI.6"}]},{"area_id":1,"description":null,"embeddable":false,"id":183550,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/183550/thumb/KhanAcademy.jpeg?1362718317","thumb_status":null,"title":"Quadratic formula","youtube_id":null,"safe_url":"http://www.khanacademy.org/exercise/quadratic_equation","contribution_name":"KhanAcademyCommonCore","grade_idents":["9","10","11","12"],"standard_idents":["A.REI.4","A.REI.4.b"],"grades_range":"9-12","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Algebra","Measurement & Data","Number Sense and Operations","Statistics and Probability"],"grades":[{"grade":"9"},{"grade":"10"},{"grade":"11"},{"grade":"12"}],"standards":[{"identifier":"A.CED.1"},{"identifier":"N.CN.7"},{"identifier":"S.ID.6"},{"identifier":"S.ID.6.a"},{"identifier":"A.REI.4"},{"identifier":"A.REI.4.b"}]},{"area_id":1,"description":null,"embeddable":false,"id":183567,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/183567/thumb/KhanAcademy.jpeg?1362719344","thumb_status":null,"title":"Equation of a hyperbola","youtube_id":null,"safe_url":"http://www.khanacademy.org/exercise/equation_of_a_hyperbola","contribution_name":"KhanAcademyCommonCore","grade_idents":["9","10","11","12"],"standard_idents":["G.GPE.3"],"grades_range":"9-12","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Geometry"],"grades":[{"grade":"9"},{"grade":"10"},{"grade":"11"},{"grade":"12"}],"standards":[{"identifier":"G.GPE.3"}]},{"area_id":1,"description":null,"embeddable":false,"id":183568,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/183568/thumb/KhanAcademy.jpeg?1362718304","thumb_status":null,"title":"Equation of an ellipse","youtube_id":null,"safe_url":"http://www.khanacademy.org/exercise/equation_of_an_ellipse","contribution_name":"KhanAcademyCommonCore","grade_idents":["9","10","11","12"],"standard_idents":["G.GPE.3"],"grades_range":"9-12","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Geometry"],"grades":[{"grade":"9"},{"grade":"10"},{"grade":"11"},{"grade":"12"}],"standards":[{"identifier":"G.GPE.3"}]},{"area_id":1,"description":null,"embeddable":false,"id":183633,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/183633/thumb/KhanAcademy.jpeg?1362718833","thumb_status":null,"title":"Radical equations","youtube_id":null,"safe_url":"http://www.khanacademy.org/exercise/radical_equations","contribution_name":"KhanAcademyCommonCore","grade_idents":["9","10","11","12"],"standard_idents":["A.REI.2"],"grades_range":"9-12","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Algebra"],"grades":[{"grade":"9"},{"grade":"10"},{"grade":"11"},{"grade":"12"}],"standards":[{"identifier":"A.REI.2"}]},{"area_id":null,"description":null,"embeddable":false,"id":400454,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/400454/thumb/KhanAcademy.jpeg?1376094700","thumb_status":null,"title":"Systems of equations","youtube_id":null,"safe_url":"https://www.khanacademy.org/exercise/systems_of_equations","contribution_name":"KhanAcademyCommonCore","grade_idents":["8","9","10","11","12"],"standard_idents":["8.EE.8","8.EE.8.a","8.EE.8.b","A.REI.6"],"grades_range":"8-12","resource_type_title":"Exercise","area_title":null,"subject_titles":["Algebra"],"grades":[{"grade":"8"},{"grade":"9"},{"grade":"10"},{"grade":"11"},{"grade":"12"}],"standards":[{"identifier":"8.EE.8"},{"identifier":"8.EE.8.a"},{"identifier":"8.EE.8.b"},{"identifier":"A.CED.3"},{"identifier":"A.REI.5"},{"identifier":"A.REI.6"}]},{"area_id":null,"description":null,"embeddable":false,"id":400568,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/400568/thumb/KhanAcademy.jpeg?1376094097","thumb_status":null,"title":"Radical equations","youtube_id":null,"safe_url":"https://www.khanacademy.org/exercise/radical_equations","contribution_name":"KhanAcademyCommonCore","grade_idents":["9","10","11","12"],"standard_idents":["A.SSE.2"],"grades_range":"9-12","resource_type_title":"Exercise","area_title":null,"subject_titles":["Algebra"],"grades":[{"grade":"9"},{"grade":"10"},{"grade":"11"},{"grade":"12"}],"standards":[{"identifier":"A.SSE.2"}]},{"area_id":null,"description":null,"embeddable":false,"id":400599,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/400599/thumb/KhanAcademy.jpeg?1376094359","thumb_status":null,"title":"Quadratic formula","youtube_id":null,"safe_url":"https://www.khanacademy.org/exercise/quadratic_equation","contribution_name":"KhanAcademyCommonCore","grade_idents":["9","10","11","12"],"standard_idents":["A.REI.4","A.REI.4.b"],"grades_range":"9-12","resource_type_title":"Exercise","area_title":null,"subject_titles":["Algebra"],"grades":[{"grade":"9"},{"grade":"10"},{"grade":"11"},{"grade":"12"}],"standards":[{"identifier":"A.REI.4"},{"identifier":"A.REI.4.b"}]},{"area_id":null,"description":null,"embeddable":false,"id":227544,"imported_area_id":42,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/227544/thumb/favicon.png?1370844647","thumb_status":null,"title":"Solving a Quadratic\r\nEquation with No Solutions by Graphing","youtube_id":null,"safe_url":"http://braingenie.ck12.org/skills/107145","contribution_name":"BrainGenie","grade_idents":[],"standard_idents":[],"grades_range":"","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Functions"],"grades":[],"standards":[]},{"area_id":null,"description":null,"embeddable":false,"id":228310,"imported_area_id":43,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/228310/thumb/favicon.png?1370833235","thumb_status":null,"title":"Solving Quadratic\r\nEquations with Imaginary Roots","youtube_id":null,"safe_url":"http://braingenie.ck12.org/skills/106846","contribution_name":"BrainGenie","grade_idents":[],"standard_idents":[],"grades_range":"","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Algebra"],"grades":[],"standards":[{"identifier":"N.CN.7"}]},{"area_id":null,"description":null,"embeddable":true,"id":337743,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/337743/thumb/bSInc7aZUkQ.?1373624268","thumb_status":null,"title":"Translate Words Into Equations","youtube_id":"bSInc7aZUkQ","safe_url":"https://www.youtube.com/watch?v=bSInc7aZUkQ","contribution_name":"YouTubeMrAlmeida","grade_idents":[],"standard_idents":[],"grades_range":"","resource_type_title":"Video","area_title":null,"subject_titles":[],"grades":[],"standards":[]},{"area_id":null,"description":null,"embeddable":false,"id":229149,"imported_area_id":44,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/229149/thumb/favicon.png?1370836664","thumb_status":null,"title":"Use the quadratic formula to solve the quadratic\r\nequation","youtube_id":null,"safe_url":"http://braingenie.ck12.org/skills/106037","contribution_name":"BrainGenie","grade_idents":[],"standard_idents":[],"grades_range":"","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Functions"],"grades":[],"standards":[]},{"area_id":null,"description":null,"embeddable":false,"id":229484,"imported_area_id":44,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/229484/thumb/favicon.png?1370838681","thumb_status":null,"title":"Solve Trigonometric Equations by Factoring a Quadratic Equation","youtube_id":null,"safe_url":"http://braingenie.ck12.org/skills/106426","contribution_name":"BrainGenie","grade_idents":[],"standard_idents":[],"grades_range":"","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Trigonometry"],"grades":[],"standards":[{"identifier":"F.IF.8.a"},{"identifier":"A.SSE.3.a"}]},{"area_id":null,"description":null,"embeddable":false,"id":224687,"imported_area_id":40,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/224687/thumb/favicon.png?1370861574","thumb_status":null,"title":"Find the incorrect\r\nequations","youtube_id":null,"safe_url":"http://braingenie.ck12.org/skills/103020","contribution_name":"BrainGenie","grade_idents":[],"standard_idents":[],"grades_range":"","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Number Sense and Operations"],"grades":[],"standards":[]},{"area_id":null,"description":null,"embeddable":false,"id":226151,"imported_area_id":41,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/226151/thumb/favicon.png?1370841976","thumb_status":null,"title":"Harder Simultaneous Equations","youtube_id":null,"safe_url":"http://braingenie.ck12.org/skills/103460","contribution_name":"BrainGenie","grade_idents":[],"standard_idents":[],"grades_range":"","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Algebra"],"grades":[],"standards":[]}]
```

As another example you can search for resources matching a specific standard or standards with the following:

` https://api.opened.io/resources.json?standard=K.CC.1 `

will return

```json
[{"description":"This is a simple video counting to thirty. Large colored numbers are shown on a black screen while an instructor says the number.\u00a0 Run time 01:06.","embeddable":true,"id":110014,"thumb":"https://opened.s3.amazonaws.com/pictures/110014/thumb/Kv-2mH3vLqI.?1359197687","title":"Counting to Thirty \r ","safe_url":"https://www.youtube.com/watch?v=Kv-2mH3vLqI","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K","1","2"],"standard_idents":["K.CC.1"],"grades_range":"K-2","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations"],"grades":[{"grade":"K"},{"grade":"1"},{"grade":"2"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.2"},{"identifier":"K.CC.4.a"},{"identifier":"K.CC.4.b"},{"identifier":"K.CC.4.c"}]},{"description":"In this 8-lesson unit students use buttons to explore logical and numerical relationships that form the conceptual basis for understanding addition and subtraction operations. Topics include counting, ordinal numbers (and relative position), classification (attributes), relationships between numbers, addition of sets, commutativity of addition, sums to 10, fact families (including subtraction), three models of subtraction (\"take away\", comparative, missing addend), and bar graphs. Includes student activity sheets and a link to an online graphing applet.","embeddable":false,"id":383276,"thumb":"https://opened.s3.amazonaws.com/pictures/383276/thumb/learning-registry-logo.png?1375303882","title":"Begin With Buttons","safe_url":"http://illuminations.nctm.org/LessonDetail.aspx?ID=U31","contribution_name":"LearningRegistry","grade_idents":["K","1","2"],"standard_idents":["K.CC.1","K.CC.3","K.CC.4","K.CC.4.a","K.CC.4.b","K.CC.4.c","K.CC.5","K.CC.6","K.CC.7","K.MD.3","K.OA.1","K.OA.2","K.OA.3","K.OA.4","K.OA.5","1.MD.4","1.OA.1","1.OA.3","1.OA.4","1.OA.5","1.OA.6","1.OA.8","2.MD.10"],"grades_range":"K-2","resource_type_title":null,"area_title":null,"subject_titles":["Measurement & Data","Number Sense and Operations"],"grades":[{"grade":"K"},{"grade":"1"},{"grade":"2"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.3"},{"identifier":"K.CC.4"},{"identifier":"K.CC.4.a"},{"identifier":"K.CC.4.b"},{"identifier":"K.CC.4.c"},{"identifier":"K.CC.5"},{"identifier":"K.CC.6"},{"identifier":"K.CC.7"},{"identifier":"K.MD.3"},{"identifier":"K.OA.1"},{"identifier":"K.OA.2"},{"identifier":"K.OA.3"},{"identifier":"K.OA.4"},{"identifier":"K.OA.5"},{"identifier":"1.MD.4"},{"identifier":"1.OA.1"},{"identifier":"1.OA.3"},{"identifier":"1.OA.4"},{"identifier":"1.OA.5"},{"identifier":"1.OA.6"},{"identifier":"1.OA.8"},{"identifier":"2.MD.10"}]},{"description":"This song is an introduction to the four most frequently used U.S. coins and their value (penny, nickel, dime, quarter). \u00a0It also shows how many of each are needed to make a dollar.","embeddable":true,"id":202896,"thumb":"https://opened.s3.amazonaws.com/pictures/202896/thumb/-SGDAMKtHTE.?1367974320","title":"The Coin Song","safe_url":"https://www.youtube.com/watch?v=-SGDAMKtHTE","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K","1","2","3","4","5"],"standard_idents":["K.CC.1","K.MD.3","2.NBT.2"],"grades_range":"K-5","resource_type_title":null,"area_title":null,"subject_titles":["Measurement & Data","Number Sense and Operations"],"grades":[{"grade":"K"},{"grade":"1"},{"grade":"2"},{"grade":"3"},{"grade":"4"},{"grade":"5"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.MD.3"},{"identifier":"1.MD.4"},{"identifier":"1.NBT.2"},{"identifier":"2.NBT.1"},{"identifier":"2.NBT.2"}]},{"description":"This is a very entertaining video and it is sure to keep your child's attention while he/she learns at the same time. Run time 01:32.","embeddable":true,"id":110711,"thumb":"https://opened.s3.amazonaws.com/pictures/110711/thumb/pQus-n4zZM8.?1359198210","title":"Count to Five with the Pig Puppet\r ","safe_url":"https://www.youtube.com/watch?v=pQus-n4zZM8","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K","1"],"standard_idents":["K.CC.1","K.CC.4","K.CC.5"],"grades_range":"K-1","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations","Other Maths"],"grades":[{"grade":"K"},{"grade":"1"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.4"},{"identifier":"K.CC.5"}]},{"description":"This is a classic\u00a0Sesame Street\u00a0video about an excited kid who turns\u00a0six years old.","embeddable":true,"id":40087,"thumb":"https://opened.s3.amazonaws.com/pictures/40087/thumb/5zkxjvJK8Eg.jpg?1376570380","title":"Sesame Street - I'm Six Years Old Today!","safe_url":"https://www.youtube.com/watch?v=5zkxjvJK8Eg","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K","1"],"standard_idents":["K.CC.1","K.CC.4"],"grades_range":"K-1","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations"],"grades":[{"grade":"K"},{"grade":"1"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.4"}]},{"description":"In this clip early learners can learn numbers through the use of ordinary objects to help count and group things together.\u00a0 The number five is shown as a numeral with various objects that are grouped in fives and counted.","embeddable":true,"id":202834,"thumb":"https://opened.s3.amazonaws.com/pictures/202834/thumb/KkoyAt1Ae8o.?1367974559","title":"Starfall Number Five","safe_url":"https://www.youtube.com/watch?v=KkoyAt1Ae8o","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K","1"],"standard_idents":["K.CC.1","K.CC.4","K.CC.5"],"grades_range":"K-1","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations","Other Maths"],"grades":[{"grade":"K"},{"grade":"1"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.4"},{"identifier":"K.CC.5"}]},{"description":"How many animals are at the Zoo? Count along and find out!\r\n\r\nFor more fun games and videos for your preschooler in a safe, child-friendly environment, visit us at http://www.sesamestreet.org\r\n\r\nSesame Street is a production of Sesame Workshop, a nonprofit educational organization which also produces Pinky Dinky Doo, The Electric Company, and other programs for children around the world.","embeddable":true,"id":64351,"thumb":"https://opened.s3.amazonaws.com/pictures/64351/thumb/ZEutPDxj8Lk.jpg?1376599954","title":"Sesame Street: 1-5 Counting Zoo Animals","safe_url":"https://www.youtube.com/watch?v=ZEutPDxj8Lk","contribution_name":"YouTube","grade_idents":["K"],"standard_idents":["K.CC.1","K.CC.2","K.CC.4","K.CC.4.a","K.CC.4.b","K.CC.5"],"grades_range":"K","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations"],"grades":[{"grade":"K"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.2"},{"identifier":"K.CC.4"},{"identifier":"K.CC.4.a"},{"identifier":"K.CC.4.b"},{"identifier":"K.CC.4.c"},{"identifier":"K.CC.5"}]},{"description":"The jumping bean shows how to divide by the number 2 in this simply-animated video. Demonstration is accompanied by a catchy tune.","embeddable":true,"id":180973,"thumb":"https://opened.s3.amazonaws.com/pictures/180973/thumb/gpI9Ro3OfY4.?1360829969","title":"Dividing by 2 by Peter Weatherall\r ","safe_url":"https://www.youtube.com/watch?v=gpI9Ro3OfY4","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K","1","2","3"],"standard_idents":["K.CC.1","K.MD.3","2.OA.3"],"grades_range":"K-3","resource_type_title":null,"area_title":null,"subject_titles":["Measurement & Data","Number Sense and Operations","Algebra"],"grades":[{"grade":"K"},{"grade":"1"},{"grade":"2"},{"grade":"3"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.6"},{"identifier":"K.MD.3"},{"identifier":"1.MD.4"},{"identifier":"1.OA.1"},{"identifier":"2.MD.10"},{"identifier":"2.OA.1"},{"identifier":"2.OA.3"}]},{"description":"In this video snippet from \"Sesame Street\", animated dancing numbers sing the song \"One\" from \"A Chorus Line\". The number 1 is the \"lead dancer/singer\", while the other numbers (2-10) serve as the chorus for the song.","embeddable":true,"id":70351,"thumb":"https://opened.s3.amazonaws.com/pictures/70351/thumb/70351.jpg?1377131256","title":"Number 1 - Sesame Street","safe_url":"https://www.youtube.com/watch?v=WRuv2ykXMIo","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K","1"],"standard_idents":["K.CC.1"],"grades_range":"K-1","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations","Other Maths"],"grades":[{"grade":"K"},{"grade":"1"}],"standards":[{"identifier":"K.CC.1"}]},{"description":"An icicle and an igloo make the number five in this Sesame Street cartoon snippet. (:16)","embeddable":true,"id":202894,"thumb":"https://opened.s3.amazonaws.com/pictures/202894/thumb/Jy4k3SpDTlU.?1367974756","title":"The Number 5","safe_url":"https://www.youtube.com/watch?v=Jy4k3SpDTlU","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K"],"standard_idents":["K.CC.1","K.CC.4"],"grades_range":"K","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations","Other Maths"],"grades":[{"grade":"K"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.4"}]},{"description":null,"embeddable":false,"id":242909,"thumb":"https://opened.s3.amazonaws.com/pictures/242909/thumb/ixl-logo.png?1372381600","title":"Numbers and counting up to 3: Count by typing - up to 3 (Kindergarten - A.3)","safe_url":"http://www.ixl.com/math/kindergarten/count-by-typing-up-to-3","contribution_name":"Ixl","grade_idents":["K"],"standard_idents":["K.CC.1","K.CC.4","K.CC.4.a","K.CC.5"],"grades_range":"K","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations"],"grades":[{"grade":"K"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.4"},{"identifier":"K.CC.4.a"},{"identifier":"K.CC.5"}]},{"description":"This intereactive Flash applet helps children learn grouping, tally marks, place value, addition, and subtraction. Students help the alien spaceship move cows into corrals by counting by 5s and 10s. They also can apply those grouping skills to practice adding and subtracting two-digit numbers with regrouping. Audio cues and prompts reinforce the user's actions and facilitate counting and the development of math language.","embeddable":false,"id":383295,"thumb":"https://opened.s3.amazonaws.com/pictures/383295/thumb/learning-registry-logo.png?1375304042","title":"Grouping and Grazing","safe_url":"http://illuminations.nctm.org/ActivityDetail.aspx?ID=218","contribution_name":"LearningRegistry","grade_idents":["K","1","2"],"standard_idents":["K.CC.1","K.CC.4","K.CC.4.a","K.CC.4.b","K.CC.4.c","K.CC.5","K.OA.1","K.OA.2","K.OA.4","1.NBT.2","1.NBT.4","1.OA.5","2.NBT.2","2.NBT.5","2.OA.1"],"grades_range":"K-2","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations"],"grades":[{"grade":"K"},{"grade":"1"},{"grade":"2"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.2"},{"identifier":"K.CC.3"},{"identifier":"K.CC.4"},{"identifier":"K.CC.4.a"},{"identifier":"K.CC.4.b"},{"identifier":"K.CC.4.c"},{"identifier":"K.CC.5"},{"identifier":"K.NBT.1"},{"identifier":"K.OA.1"},{"identifier":"K.OA.2"},{"identifier":"K.OA.4"},{"identifier":"1.NBT.2"},{"identifier":"1.NBT.4"},{"identifier":"1.OA.5"},{"identifier":"2.NBT.2"},{"identifier":"2.NBT.5"},{"identifier":"2.OA.1"}]},{"description":"The song \"Five Little Monkeys\" is sung with accompanying animation in this cartoon. Count along while the monkeys jump on and fall off the bed. Introduces the concept of \"no more.\"","embeddable":true,"id":110712,"thumb":"https://opened.s3.amazonaws.com/pictures/110712/thumb/ZhODBFQ2-bQ.?1359193736","title":" Count to Five with the Five Little Monkeys Song","safe_url":"https://www.youtube.com/watch?v=ZhODBFQ2-bQ","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K","1","2","3","4"],"standard_idents":["K.CC.1","K.CC.4","K.CC.5"],"grades_range":"K-4","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations","Speaking and Listening","Other Maths"],"grades":[{"grade":"K"},{"grade":"1"},{"grade":"2"},{"grade":"3"},{"grade":"4"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.4"},{"identifier":"K.CC.5"}]},{"description":"This animated musical video by Peter Weatherall demonstrates with a jumping bean how to subtract using the number line. This simply-animated video explores only\u00a0one basic problem: 10-5=5.","embeddable":true,"id":180964,"thumb":"https://opened.s3.amazonaws.com/pictures/180964/thumb/VZh6p3kUdyA.?1360830319","title":"Number Line Subtraction Song","safe_url":"https://www.youtube.com/watch?v=VZh6p3kUdyA","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K","1","2","3","4"],"standard_idents":["K.CC.1"],"grades_range":"K-4","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations","Algebra"],"grades":[{"grade":"K"},{"grade":"1"},{"grade":"2"},{"grade":"3"},{"grade":"4"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.4"},{"identifier":"K.CC.7"},{"identifier":"K.OA.1"},{"identifier":"K.OA.2"},{"identifier":"K.OA.5"}]},{"description":"Ten bones are hidden in the squares of a blank 1-100 grid. Students are given the numbers of the squares one at a time. They attempt to locate the numbers in the hundreds chart and find all 10 bones within 60 seconds. Numbers of the incorrectly guessed squares are left in place to help with the search. The game helps students understand the structure and patterns of our base-10 number system. Children can be encouraged to make use of a found bone to locate the next one.","embeddable":false,"id":383181,"thumb":"https://opened.s3.amazonaws.com/pictures/383181/thumb/learning-registry-logo.png?1375305340","title":"Give the Dog a Bone","safe_url":"http://www.oswego.org/ocsd-web/games/DogBone/gamebone.html","contribution_name":"LearningRegistry","grade_idents":["K","1","2"],"standard_idents":["K.CC.1","K.CC.2","1.NBT.2","1.NBT.5"],"grades_range":"K-2","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations"],"grades":[{"grade":"K"},{"grade":"1"},{"grade":"2"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.2"},{"identifier":"1.NBT.2"},{"identifier":"1.NBT.5"}]},{"description":null,"embeddable":false,"id":242914,"thumb":"https://opened.s3.amazonaws.com/pictures/242914/thumb/ixl-logo.png?1372382038","title":"Numbers and counting up to 20: Count to 20 (Kindergarten - D.1)","safe_url":"http://www.ixl.com/math/kindergarten/count-to-20","contribution_name":"Ixl","grade_idents":["K"],"standard_idents":["K.CC.1","K.CC.4","K.CC.4.a","K.CC.4.b","K.CC.5"],"grades_range":"K","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations"],"grades":[{"grade":"K"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.4"},{"identifier":"K.CC.4.a"},{"identifier":"K.CC.4.b"},{"identifier":"K.CC.5"}]},{"description":"Get this song in iTunes: http://bit.ly/A3OKVJ New Video: What Time Is It? http://youtu.be/0Yq_rztquuU\nLet's Count to 100 together! If you have a class or friends, get a partner and play rock, scissors, paper! \n\nGet this video in an App!\nKids Songs in English iPhone and iPad App: 5 Great Videos in a fun kids App!\niPhone App: http://itunes.apple.com/us/app/kids-songs-in-english/id476263774?mt=8\niPad App: http://itunes.apple.com/us/app/kids-songs-in-english-hd/id476264101?mt=8\nKids! Play the Sounds Right Online Game and test your numbers! http://www.dreamenglish.com/games/numbers\nCreated by Cambridge English Online!\n\nThis song is available in the Dream English Song Download Special Pack, please check it out here:\nhttp://www.dreamenglish.com/shop\nIf you need to know how to play the rock, scissors, paper hand game read this page:\nhttp://www.dreamenglish.com/rockscissorspaper\n\nhttp://www.dreamenglish.com\nJoin us on facebook:\nhttp://www.facebook.com/dreamenglish","embeddable":true,"id":75909,"thumb":"https://opened.s3.amazonaws.com/pictures/75909/thumb/default.jpg?1357576628","title":"Count to 100! Count from 1 to 100 Song","safe_url":"https://www.youtube.com/watch?v=rG_uUws1oC0","contribution_name":"YouTube","grade_idents":["K"],"standard_idents":["K.CC.1","K.CC.2"],"grades_range":"K","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations"],"grades":[{"grade":"K"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.2"},{"identifier":"K.CC.3"},{"identifier":"K.CC.4.a"},{"identifier":"K.CC.4.b"},{"identifier":"K.CC.4.c"},{"identifier":"2.NBT.1.a"}]},{"description":"A fun little sesame street video showing basic subtraction practice using a gumball machine.","embeddable":true,"id":183803,"thumb":"https://opened.s3.amazonaws.com/pictures/183803/thumb/ern4WWE6TUw.?1362805606","title":"Gumball Subtraction - Sesame Street","safe_url":"https://www.youtube.com/watch?v=ern4WWE6TUw","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K","1","2"],"standard_idents":["K.CC.1","K.CC.4","K.MD.3","K.OA.1","K.OA.2","1.OA.1"],"grades_range":"K-2","resource_type_title":null,"area_title":null,"subject_titles":["Measurement & Data","Number Sense and Operations","Algebra"],"grades":[{"grade":"K"},{"grade":"1"},{"grade":"2"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.4"},{"identifier":"K.CC.5"},{"identifier":"K.CC.6"},{"identifier":"K.MD.3"},{"identifier":"K.OA.1"},{"identifier":"K.OA.2"},{"identifier":"1.MD.2"},{"identifier":"1.OA.1"}]},{"description":"Snippet begins with a short ad. Children count to 10 and then back from 10. \u00a0The live action movie then focuses on counting things in groups of three.","embeddable":false,"id":187563,"thumb":"https://opened.s3.amazonaws.com/pictures/187563/thumb/11306885.?1364826932","title":"Counting Three Objects","safe_url":"https://secure.hulu.com/embed/W9aqyYfCsEslfBU5ia4Mpg","contribution_name":"WatchKnowLearnCommonCore","grade_idents":["K","1"],"standard_idents":["K.CC.1","K.CC.4"],"grades_range":"K-1","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations"],"grades":[{"grade":"K"},{"grade":"1"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.2"},{"identifier":"K.CC.4"},{"identifier":"K.CC.4.a"},{"identifier":"K.CC.4.b"},{"identifier":"K.CC.4.c"},{"identifier":"K.CC.7"},{"identifier":"K.G.1"}]},{"description":null,"embeddable":false,"id":242912,"thumb":"https://opened.s3.amazonaws.com/pictures/242912/thumb/ixl-logo.png?1372381724","title":"Numbers and counting up to 10: Count to 10 (Kindergarten - C.1)","safe_url":"http://www.ixl.com/math/kindergarten/count-to-10","contribution_name":"Ixl","grade_idents":["K"],"standard_idents":["K.CC.1","K.CC.4","K.CC.4.a","K.CC.4.b","K.CC.5"],"grades_range":"K","resource_type_title":null,"area_title":null,"subject_titles":["Number Sense and Operations"],"grades":[{"grade":"K"}],"standards":[{"identifier":"K.CC.1"},{"identifier":"K.CC.4"},{"identifier":"K.CC.4.a"},{"identifier":"K.CC.4.b"},{"identifier":"K.CC.5"}]}]
```

Show Resource 
-------------

Show information for a specific resource, based on the OpenEd resource ID (a unique integer)

For example:

` https://api.opened.io/resources/183426.json `

will return

```json
{"area_id":1,"description":null,"embeddable":false,"id":183426,"imported_area_id":null,"imported_subject_id":null,"is_patched":null,"thumb":"https://opened.s3.amazonaws.com/pictures/183426/thumb/KhanAcademy.jpeg?1362719117","thumb_status":null,"title":"Systems of equations","youtube_id":null,"safe_url":"http://www.khanacademy.org/exercise/systems_of_equations","contribution_name":"KhanAcademyCommonCore","grade_idents":["8","9","10","11","12"],"standard_idents":["8.EE.8","8.EE.8.a","8.EE.8.b","8.EE.8.c","A.CED.3","A.REI.6"],"grades_range":"8-12","resource_type_title":"Exercise","area_title":"Mathematics","subject_titles":["Algebra"],"grades":[{"grade":"8"},{"grade":"9"},{"grade":"10"},{"grade":"11"},{"grade":"12"}],"standards":[{"identifier":"8.EE.8"},{"identifier":"8.EE.8.a"},{"identifier":"8.EE.8.b"},{"identifier":"8.EE.8.c"},{"identifier":"A.CED.3"},{"identifier":"A.REI.5"},{"identifier":"A.REI.6"}]}
```
