<template>
  <div>
    <form>
      <table cellspacing="3" width="700" border="1">
        <tr>
          <td width=20%>
            <p align="center">{{name}}</p>
          </td>
          <td width="80%" align="left">
            <img :style="{ width: `${electPer * 5}px`, height:'20px'}" class="barImgae" src="../assets/bar.png" /> {{
            electPer
            }}
          </td>
        </tr>

        <!-- <% double sum=0; while(rset.next()){ sum +=rset.getInt(3); } rset=stmt.executeQuery("select
          hubo.kiho,hubo.name, ifnull(tupyoCount,0) from hubo left outer join (select kiho, count(*) as tupyoCount
          from tupyo group by kiho) tupyoCount on hubo.kiho=tupyoCount.kiho;"); while(rset.next()){ double
          per=(rset.getInt(3)/sum)*100; double perRound=Math.round(per*100) /100.0; out.print("<tr>
          <td width=200><a href=C_02_H.jsp?name="+rset.getString(2)+" &kiho="+ rset.getInt(1) +">
              <p align=center>"+ rset.getString(2)+ "</p>
            </a></td>");
          out.print("<td width=500<p align=left><img src=bar.png width="+ perRound*4  + " height=20>"+
            Integer.toString(rset.getInt(3)) +"("+ perRound +"%)"+ "</p></a></td>
          </tr>");
          }
          rset.close();
          stmt.close();
          conn.close();
          %> -->

      </table>


    </form>
  </div>
</template>
<script>
export default {
  name: "ResultViewa",
  props: {
    name: String,
    electPer: Number,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<!-- <style lang="scss" scoped>

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style> -->