# Winter of Code - Leaderboard

```jsx
/*react*/
<style>
</style>
<script>
  export default class Application extends React.Component {
    constructor(props) {
      super(props)
      this.state = {
        data: []
      }
    }
    componentWillMount () {
      fetch('https://wocleaderboard-backend.herokuapp.com/getLeaderBoard')
        .then(response => response.json())
        .then(data => this.setState({ data: data}));
    }
    render() {
      console.log(this.state.data);
      return (
        <div>
          <table style={{"width" : "100%"}}>
            <tr>
              <th>Github Username</th>
              <th>Score</th>
            </tr>
            {
            this.state.data.map((el) => {
              return (
              <tr>
                <td><a href={"https://github.com/" + el.key}>{el.key}</a></td>
                <td>{Math.abs(el.score)}</td>
              </tr>
              )
            })
            }
          </table>
        </div>
      )
    }
  }
```
