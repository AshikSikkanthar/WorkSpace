import React from "react";
const couterfun = (WrappedComponent,incrementValue) => 
{
    class CountFun extends React.Component 
    {

        constructor(props) 
        {
            super(props);
      
            this.state = {
              count: 0,
            };
          }

          increment = () => {
            this.setState((prevState) => {
              return { count: prevState.count + incrementValue  };
            });
          };

          render() {
            return (
              <WrappedComponent
                name="Ashik"
                count={this.state.count}
                increment={this.increment}
                {...this.props}
              />
            );
          }
        }
   

        return CountFun;
      };
       

    


export default couterfun;
