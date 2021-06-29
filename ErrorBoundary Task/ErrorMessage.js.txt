import React, { Component } from "react";

class ErrorMessage extends Component {
  constructor(props) {
    super(props);

    this.state = {
      hasError: false,
    };
  }

  static getDerivedStateFromError(error){
    return{
        hasError:true
    }
  }

  componentDidCatch(error,info){
      console.log(error)
      console.log(info)
  }

  render() {
    if(this.state.hasError){
        return<div><b>Oops...!!!</b> <h1>Something went wrong</h1></div>
    }
    return this.props.children;
  }
}

export default ErrorMessage;