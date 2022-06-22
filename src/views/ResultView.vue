<template>
  <div>
    <h1>후보별 득표율</h1>
    <form action="">
      <table cellspacing=1 width=400 border=1>
        <tr>
          <td height=50 width=100 align="center"><a href="A_01_H.jsp">후보등록</a></td>
          <td height=50 width=100 align="center"><a href="B_01_H.jsp">투표</a></td>
          <td height=50 width=100 bgcolor="#00FFFF" align="center"><a href="result">개표결과</a></td>
        </tr>
      </table>

      <ResultViewa name="asdasd" />
      <!-- <% Class.forName("com.mysql.jdbc.Driver"); Connection
      conn=DriverManager.getConnection("jdbc:mysql://localhost/koposw44","root","koposw44"); Statement
      stmt=conn.createStatement(); ResultSet rset=stmt.executeQuery("select a.kiho, b.name, count(a.kiho) "+ 
                          " from tupyo as a, hubo as b " +
                          " where a.kiho=b.kiho " +
                          " group by a.kiho;"); %> -->
    </form>
  </div>
</template>
<style lang="scss" scoped>
.about {
  .msg {
    font-size: "13px";
    color: red;
  }
}
</style>
<script>
// @ is an alias to /src
import ResultViewa from "@/components/ResultViewa.vue";

export default {
  name: "ResultViewa",
  components: {
    ResultViewa,
  },
};
</script>