# Snapshot report for `tests/index.test.js`

The actual snapshot is saved in `index.test.js.snap`.

Generated by [AVA](https://ava.li).

## should return correct Scala Case Class

> Snapshot 1

    `case class Friends (␊
      id: Int,␊
      name: String␊
    )␊
    ␊
    case class Hello (␊
      _id: String,␊
      type: Double,␊
      "a b": String,␊
      longitude: Double,␊
      tags: Seq[String],␊
      "#friends": Seq[Friends]␊
    )␊
    ␊
    case class RootInterface (␊
      hello: Seq[Hello]␊
    )␊
    ␊
    `

## should return correct Typings when objects have different keys in an Array

> Snapshot 1

    `type RootInterface =  {␊
      x: X[],␊
    };␊
    ␊
    type X =  {␊
      a: string,␊
      b?: string,␊
      c?: string,␊
    };␊
    ␊
    `

## should return correct flow typings

> Snapshot 1

    `type Friends =  {␊
      id: number,␊
      name: string,␊
    };␊
    ␊
    type Hello =  {␊
      _id: string,␊
      type: number,␊
      "a b": string,␊
      longitude: number,␊
      tags: string[],␊
      "#friends": Friends[],␊
    };␊
    ␊
    type RootInterface =  {␊
      hello: Hello[],␊
    };␊
    ␊
    `

## should return correct flow typings if array is passed

> Snapshot 1

    `type RootInterface =  {␊
      a: string,␊
      b: string,␊
    };␊
    ␊
    `

## should return correct rust-serde struct

> Snapshot 1

    `#[derive(Serialize, Deserialize)]␊
    struct Friends {␊
      id: i64,␊
      name: String,␊
    }␊
    ␊
    #[derive(Serialize, Deserialize)]␊
    struct Hello {␊
      _id: String,␊
      #[serde(rename = "type")]␊
      type_: f64,␊
      #[serde(rename = "a b")]␊
      aB_: String,␊
      longitude: f64,␊
      tags: Vec<String>,␊
      #[serde(rename = "#friends")]␊
      friends_: Vec<Friends>,␊
    }␊
    ␊
    #[derive(Serialize, Deserialize)]␊
    struct RootInterface {␊
      hello: Vec<Hello>,␊
    }␊
    ␊
    `

## should return correct typescript interfaces

> Snapshot 1

    `interface Friends {␊
      id: number;␊
      name: string;␊
    }␊
    ␊
    interface Hello {␊
      _id: string;␊
      type: number;␊
      "a b": string;␊
      longitude: number;␊
      tags: string[];␊
      "#friends": Friends[];␊
    }␊
    ␊
    interface RootInterface {␊
      hello: Hello[];␊
    }␊
    ␊
    `
