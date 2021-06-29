import React from "react";

function EmpolyeeInfo({ EmpName }) {
  if (EmpName === "Ajay") {
    throw new Error("Emp Name not correct");
  }
  return (
    <div>
      <h3>{EmpName}</h3>
    </div>
  );
}

export default EmpolyeeInfo;