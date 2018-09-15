##Using Render Props

Render props is a simple technique for sharing code between React components using a prop whose value is a function. Render props is where a component prop is assigned a function, and is called in the render method of the component. It works to help build reusable codes by taking in propTypes and is being used in different methods. When a propType is being rendered, the property is being declared like an object.
Props can be used in loading dynamic datas easily on the fly and it can be passed in as children of a parent element. It also helps to declare tha data type that is expected for it and be set as a required function. The prop is rendered in the component.

When using Props
class Todo extends Component {

  static propTypes = {
    url: PropTypes.string.isRequired,
    render: PropTypes.string.isRequired
  }

  constructor (props)
  super(props)

  this.state = {
    data:[],
    isLoading: true
  }

  render () {
    return (
    
        <Todo 
        url= 'https://jsonplaceholder.typicode.com/todos'

        //Other codes to be rendered goes here.
        />
      </div>
    )
  }
}


## Higher Order Functions
Higher order functions are functions that takes in a component as a parameter of a function and returns a parameter to be used in another function. When creating a function in HOC, the components passed in can take more parameters that can be used like an argument when the component is being used in another function. It helps to build functions that is well maintained and help avoid re-writing several classes.

const Todo = (TodoComponent) => {
  class todoComponent extends Component {
    constructor (props)
    super(props)

    this.state = {
      data:[],
      isLoading: true
    }

    //Other codes goes here

    render() {
      return (
        <div className="data-component">
          <ComposedComponent {...this.state} />
        </div>
      )
    }
  }
}