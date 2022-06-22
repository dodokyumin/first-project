<template>
  <div>
    <h1>후보별 득표율</h1>
    <form action="">
      <table cellspacing=1 width=400 border=1>
        <tr>
          <td height=50 width=100 align="center"><a href="A_01_H.jsp">후보등록</a></td>
          <td height=50 width=100 align="center"><a href="B_01_H.jsp">투표</a></td>
          <td height=50 width=100 bgcolor="#00FFFF" align="center"><a href="ResultView2">개표결과</a></td>
        </tr>
      </table>
      <table cellspacing="3" width="700" border="1">
        <tr>
          <td width=20%>
            <p align="center">
              이름
            </p>
          </td>
          <td width=80%>
            <p align="center">인기도</p>
          </td>
        </tr>
      </table>

      <ResultViewa name="홍길1" electPer="50" />
      <ResultViewa name="홍길2" electPer="30" />
      <ResultViewa name="홍길3" electPer="20" />
      <!-- <% Class.forName("com.mysql.jdbc.Driver"); Connection
      conn=DriverManager.getConnection("jdbc:mysql://localhost/koposw44","root","koposw44"); Statement
      stmt=conn.createStatement(); ResultSet rset=stmt.executeQuery("select a.kiho, b.name, count(a.kiho) "+ 
                          " from tupyo as a, hubo as b " +
                          " where a.kiho=b.kiho " +
                          " group by a.kiho;"); %> -->
    </form>
  </div>
</template>

<script>
// @ is an alias to /src

import ResultViewa from "@/components/ResultViewa.vue";

export default {
  name: "ResultView",
  components: {
    ResultViewa
},
  data() {
    return {
      items: [
        { name: "홍길1", electPer: 50 },
        { name: "홍길2", electPer: 30 },
        { name: "홍길3", electPer: 20 }
      ]
    }
  }
};
</script>
