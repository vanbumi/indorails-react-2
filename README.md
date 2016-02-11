# Get Started

	<script src="https://fb.me/react-0.14.7.js"></script>
	<script src="https://fb.me/JSXTransformer-0.12.2.js"></script>

## Chapter One "Hello World"

	<div id="content"></div>

	<script type="text/jsx">

		var App = React.createClass({
			render: function() {
				return <h3>Hello Dyo and Hello World!</h3>
			}
		});
		React.render(<App />, document.getElementById('content'));
	</script>	

## Chapter Two - Render Method

	<div id="container"></div>

	<script type="text/jsx">

		var App = React.createClass({
			render: function() {
				return(
					<div>
						<b>Bold</b>
						<h2>Hello Dyo!</h2>
					</div>	
				)
			}
		});
		React.render(<App />, document.getElementById('container'));
		
	</script>	

## Chapter Three - Properties

	<div id="content"></div>	

	<script type="text/jsx">

		var Proper = React.createClass({
			getDefaultProps: function() {
				return {
					txt: 'Ini adalah default text yaaa!',
					cat: 10
				}
			},
			propTypes: {
				txt: React.PropTypes.string,
				cat: React.PropTypes.number.isRequired
			},
			render: function() {
				var txt = this.props.txt
				var cat = this.props.cat
				return(
					<div>
						<h2>React Properties</h2>
						<p>{this.props.txt}</p>
						<p>{txt}</p>
						<p>{cat}</p>
					</div>
				)
			}		
		});

		// React.render(< Proper cat={5} txt="Ini adalah props text" />, document.getElementById('content'));
		React.render(< Proper />, document.getElementById('content')); 

	</script>

## Chapter Four - State Basic

	<div id="content"></div>

	<script type="text/jsx">

		var Statex = React.createClass({
			getInitialState: function() {
				return{
					txt: 'This the state'
				}	
			},
			update: function(e) {
				this.setState({txt: e.target.value});
			},
			render: function() {
				return(
					<div>
						<input type="text" onChange={this.update} />
						<h2>{this.props.statex}</h2>
						<h3>{this.state.txt}</h3>
					</div>	
				)
			}
		});

		React.render(<Statex statex="State Basic for Update & Maintain Component"/>, document.getElementById('content'));
	</script>		